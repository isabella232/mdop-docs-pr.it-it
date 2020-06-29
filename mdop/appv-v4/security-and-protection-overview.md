---
title: Panoramica di sicurezza e protezione
description: Panoramica di sicurezza e protezione
author: dansimp
ms.assetid: a43e1c53-7936-4d48-a110-0be26c8e9d97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b08b7dcb3defa8a01a4fd8a3e7234b5ac2956c4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815656"
---
# <span data-ttu-id="99543-103">Panoramica di sicurezza e protezione</span><span class="sxs-lookup"><span data-stu-id="99543-103">Security and Protection Overview</span></span>


<span data-ttu-id="99543-104">Microsoft Application Virtualization 4.5 offre le caratteristiche di sicurezza avanzate seguenti per pianificare e implementare una strategia di distribuzione più sicura:</span><span class="sxs-lookup"><span data-stu-id="99543-104">Microsoft Application Virtualization4.5 provides the following enhanced security features to help you plan and implement a more secure deployment strategy:</span></span>

-   <span data-ttu-id="99543-105">La virtualizzazione delle applicazioni ora supporta TLS (Transport Layer Security) con certificati X. 509 v3.</span><span class="sxs-lookup"><span data-stu-id="99543-105">Application Virtualization now supports Transport Layer Security (TLS) using X.509 V3 certificates.</span></span> <span data-ttu-id="99543-106">A condizione che sia stato effettuato il provisioning di un certificato server per l'Application Virtualization Management o lo streaming server previsto, l'installazione sarà predefinita per la sicurezza, usando il protocollo RTSPs sulla porta 322.</span><span class="sxs-lookup"><span data-stu-id="99543-106">Provided that a server certificate has been provisioned to the planned Application Virtualization Management or Streaming Server, the installation will default to secure, using the RTSPS protocol over port 322.</span></span> <span data-ttu-id="99543-107">L'uso di RTSPs garantisce che la comunicazione tra i server di virtualizzazione dell'applicazione e i client di virtualizzazione dell'applicazione sia firmata e crittografata</span><span class="sxs-lookup"><span data-stu-id="99543-107">Using RTSPS ensures that communication between the Application Virtualization Servers and the Application Virtualization Clients is signed and encrypted.</span></span> <span data-ttu-id="99543-108">Se al server non viene assegnato un certificato durante l'installazione di Application Virtualization Server, la comunicazione verrà impostata su RTSP sulla porta 554.</span><span class="sxs-lookup"><span data-stu-id="99543-108">If no certificate is assigned to the server during the Application Virtualization Server installation, the communication will be set to RTSP over port 554.</span></span>

    **<span data-ttu-id="99543-109">Nota sulla sicurezza:</span><span class="sxs-lookup"><span data-stu-id="99543-109">Security Note:</span></span>**

    <span data-ttu-id="99543-110">Per fornire una configurazione sicura del server, è necessario assicurarsi che le porte RTSP siano disabilitate anche se tutti i pacchetti sono configurati per l'uso di RTSPs.</span><span class="sxs-lookup"><span data-stu-id="99543-110">To help provide a secure setup of the server, you must make sure that RTSP ports are disabled even if you have all packages configured to use RTSPS.</span></span>

    <span data-ttu-id="99543-111">Se si aggiungono certificati di sicurezza al server dopo l'installazione del server, è possibile che il server non rilevi i certificati.</span><span class="sxs-lookup"><span data-stu-id="99543-111">If you add security certificates to the server after installing the server, the server might not detect the certificates.</span></span> <span data-ttu-id="99543-112">Per garantire il rilevamento del certificato di sicurezza, riavviare il server dopo l'aggiunta dei certificati.</span><span class="sxs-lookup"><span data-stu-id="99543-112">To help ensure security certificate detection, restart the server after adding the certificates.</span></span>

-   <span data-ttu-id="99543-113">Il client deve essere configurato per l'uso dello stesso protocollo e della stessa porta del server oppure non sarà in grado di comunicare con il server.</span><span class="sxs-lookup"><span data-stu-id="99543-113">The client must be configured to use the same protocol and port as the server, or it will not be able to communicate with the server.</span></span> <span data-ttu-id="99543-114">Il client deve considerare attendibile anche l'autorità emittente del certificato e le navi con diversi provider primari nell'archivio radice attendibile.</span><span class="sxs-lookup"><span data-stu-id="99543-114">The client must also trust the issuer of the certificate and ships with several of the primary providers in its Trusted Root Store.</span></span> <span data-ttu-id="99543-115">È possibile usare certificati autofirmati, ma sarà necessario aggiornare i client.</span><span class="sxs-lookup"><span data-stu-id="99543-115">You can use self-signed certificates, but you will need to update the clients.</span></span>

-   <span data-ttu-id="99543-116">Quando si configurano i server IIS per l'uso del protocollo HTTPS per lo streaming, è necessario configurare Secure Sockets Layer (SSL) nel server IIS e eseguire il provisioning del certificato per il server.</span><span class="sxs-lookup"><span data-stu-id="99543-116">When configuring IIS servers to use the HTTPS protocol for streaming, you will need to set up Secure Sockets Layer (SSL) on the IIS server and provision the certificate for the server.</span></span> <span data-ttu-id="99543-117">Anche i client dovranno essere configurati per considerare attendibile l'autorità di certificazione radice che ha emesso il certificato del server.</span><span class="sxs-lookup"><span data-stu-id="99543-117">The clients will also need to be configured to trust the root certification authority that issued the server certificate.</span></span>

-   <span data-ttu-id="99543-118">L'autenticazione Kerberos è stata aggiunta a Microsoft Application Virtualization come meccanismo di autenticazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="99543-118">Kerberos authentication has been added to Microsoft Application Virtualization as the default authentication mechanism.</span></span> <span data-ttu-id="99543-119">Le versioni precedenti si basavano su NTLM v2 per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="99543-119">Earlier versions relied upon NTLM V2 for authentication.</span></span> <span data-ttu-id="99543-120">L'uso dell'autenticazione Kerberos rafforza la sicurezza delle comunicazioni tra il client e il server di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="99543-120">Using Kerberos Authentication strengthens the security of the communication between the client and the Application Virtualization server.</span></span> <span data-ttu-id="99543-121">Quando una connessione è stata avviata dal client, il server di virtualizzazione dell'applicazione verifica il ticket di sessione con il centro distribuzione chiavi (KDC).</span><span class="sxs-lookup"><span data-stu-id="99543-121">When a connection has been initiated from the client, the Application Virtualization Server verifies the session ticket with the Key Distribution Center (KDC).</span></span>

-   <span data-ttu-id="99543-122">Dato il supporto per l'uso dei certificati server e l'uso dei protocolli RTSPs o HTTPS, ora è possibile supportare i client all'esterno della rete aziendale.</span><span class="sxs-lookup"><span data-stu-id="99543-122">Because of the support for using server certificates and using the RTSPS or HTTPS protocols, you can now support clients outside of the corporate network.</span></span> <span data-ttu-id="99543-123">In questo modo è possibile eliminare la necessità per gli utenti di dispositivi mobili di configurare una connessione sicura alla rete aziendale (VPN, RAS e così via) prima di avviare applicazioni di Application Virtualization provisioning.</span><span class="sxs-lookup"><span data-stu-id="99543-123">This can help eliminate the need for mobile users to set up a secure connection to the corporate network (VPN, RAS, and so on) prior to launching Application Virtualization provisioned applications.</span></span>

<span data-ttu-id="99543-124">Altre importanti considerazioni sulla sicurezza da tenere in considerazione includono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="99543-124">Other important security considerations to consider include the following:</span></span>

-   <span data-ttu-id="99543-125">Mantenere sempre i server completamente aggiornati e protetti.</span><span class="sxs-lookup"><span data-stu-id="99543-125">Always keep servers fully updated and protected.</span></span>

-   <span data-ttu-id="99543-126">Per aggiungere un certificato per consentire comunicazioni più sicure all'Application Virtualization Management Server, è necessario che siano soddisfatti i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="99543-126">To add a certificate to enable more secure communications to the Application Virtualization Management Server, the following criteria must be met:</span></span>

    -   <span data-ttu-id="99543-127">L'utente che aggiungerà il certificato deve essere un amministratore nel server in cui si trova l'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="99543-127">The user who will be adding the certificate must be an administrator on the server where the certificate store is located.</span></span>

    -   <span data-ttu-id="99543-128">Il servizio Server deve essere avviato.</span><span class="sxs-lookup"><span data-stu-id="99543-128">The server service must be started.</span></span>

    -   <span data-ttu-id="99543-129">La porta 139 nel server di gestione deve essere aperta al servizio Web server'sIP.</span><span class="sxs-lookup"><span data-stu-id="99543-129">Port 139 on the Management Server must be open to the Web Service server’sIP.</span></span>

-   <span data-ttu-id="99543-130">USA gli elenchi di controllo di accesso (ACL) per verificare che i pacchetti dell'applicazione e tutti i file di pacchetto siano protetti e non vengano manomessi.</span><span class="sxs-lookup"><span data-stu-id="99543-130">Use access control lists (ACLs) to ensure that the application packages and all package files are protected and cannot be tampered.</span></span> <span data-ttu-id="99543-131">Gli ACL limitano l'accesso alla posizione o alla cartella in cui vengono archiviati i pacchetti, consentendo l'accesso solo a determinati account.</span><span class="sxs-lookup"><span data-stu-id="99543-131">ACLs restrict access to the location or folder where you store the packages, allowing access only to certain accounts.</span></span>

-   <span data-ttu-id="99543-132">Verificare che il canale tra l'Application Virtualization Management Server e il database sia protetto, ad esempio tramite IPsec.</span><span class="sxs-lookup"><span data-stu-id="99543-132">Make sure that the channel between the Application Virtualization Management Server and the database is secured—for example, by using IPsec.</span></span>

-   <span data-ttu-id="99543-133">Se i pacchetti sono archiviati in una SAN o NAS, verificare che la connessione tra il dispositivo di archiviazione centrale e i server di virtualizzazione dell'applicazione sia protetta.</span><span class="sxs-lookup"><span data-stu-id="99543-133">If packages are stored on a SAN or NAS, ensure the connection between the central storage device and the Application Virtualization Servers is protected.</span></span>

-   <span data-ttu-id="99543-134">Tutti i canali di comunicazione al client devono essere protetti, incluse le connessioni al server di pubblicazione, l'Application Virtualization Server e il percorso dei file OSD e ICO, usando un protocollo come HTTPS o IPsec.</span><span class="sxs-lookup"><span data-stu-id="99543-134">All communication channels to the client should be protected—including connections to the publishing server, the Application Virtualization Server, and the path to the OSD and ICO files—by using a protocol such as HTTPS or IPsec.</span></span> 

-   <span data-ttu-id="99543-135">Le autorizzazioni client devono essere configurate per evitare che i pacchetti vengano manomessi dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="99543-135">Client permissions should be configured to help ensure that packages cannot be tampered with by users.</span></span> <span data-ttu-id="99543-136">È particolarmente importante non concedere agli utenti l'autorizzazione per l'aggiunta o l'aggiornamento di pacchetti su sistemi, ad esempio i server Host sessione Desktop remoto (host RDSession) condivisi con più utenti.</span><span class="sxs-lookup"><span data-stu-id="99543-136">It is especially important that you do not grant users permission to add or update packages on systems, such as Remote Desktop Session Host (RDSession Host) servers, that are shared with multiple users.</span></span>

-   <span data-ttu-id="99543-137">L'autenticazione Kerberos deve essere consentita in ambienti di dominio o di foresta per consentire il corretto funzionamento della console di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="99543-137">Kerberos authentication must be permitted across domain or forest environments for the Server Management Console to work correctly.</span></span>

-   <span data-ttu-id="99543-138">Questa versione del software non supporta l'hosting di un server RTSP basato su Kerberos e di un server IIS basato solo su Microsoft NTLM nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="99543-138">This release of the software does not support hosting a Kerberos-based RTSP server and a Microsoft NTLM-only-based IIS server on the same computer.</span></span> <span data-ttu-id="99543-139">Per ospitare un server RTSP e un server IIS nello stesso computer, rimuovere l'SPN dal server IIS e usare l'autenticazione NTLM.</span><span class="sxs-lookup"><span data-stu-id="99543-139">To host an RTSP server and an IIS server on the same computer, remove the SPN from the IIS server and use NTLM authentication.</span></span>

## <span data-ttu-id="99543-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99543-140">Related topics</span></span>


[<span data-ttu-id="99543-141">Pianificazione della distribuzione del sistema Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="99543-141">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





