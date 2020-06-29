---
title: Installazione sicura di App-V Management Server o Streaming Server
description: Installazione sicura di App-V Management Server o Streaming Server
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816326"
---
# <span data-ttu-id="db12a-103">Installazione sicura di App-V Management Server o Streaming Server</span><span class="sxs-lookup"><span data-stu-id="db12a-103">Installing App-V Management Server or Streaming Server Securely</span></span>


<span data-ttu-id="db12a-104">Gli argomenti di questa sezione includono informazioni per l'installazione di una versione di sicurezza avanzata di App-V Management Server o App-V Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="db12a-104">The topics in this section provide information for installing an enhanced security version of the App-V Management Server or the App-V Streaming Server.</span></span>

<span data-ttu-id="db12a-105">**Nota**  L'installazione o la configurazione di un'app-V Management o di un server di streaming per l'uso della sicurezza avanzata (ad esempio, Transport Layer Security o TLS) richiede che un certificato X. 509 v3 sia stato provisionato nel server App-V.</span><span class="sxs-lookup"><span data-stu-id="db12a-105">**Note** Installing or configuring an App-V Management or Streaming Server to use enhanced security (for example, Transport Layer Security, or TLS) requires that an X.509 V3 certificate has been provisioned to the App-V server.</span></span>

 

<span data-ttu-id="db12a-106">Quando si prepara l'installazione o la configurazione di una gestione sicura o di un server di flusso, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="db12a-106">When you prepare to install or configure a secure Management or Streaming Server, consider the following technical requirements:</span></span>

-   <span data-ttu-id="db12a-107">Il certificato deve essere valido.</span><span class="sxs-lookup"><span data-stu-id="db12a-107">The certificate must be valid.</span></span> <span data-ttu-id="db12a-108">Se il certificato non è valido, il client termina la connessione.</span><span class="sxs-lookup"><span data-stu-id="db12a-108">If the certificate is not valid, the client ends the connection.</span></span>

-   <span data-ttu-id="db12a-109">Il certificato deve contenere l'utilizzo corretto della *chiave avanzata* (EKU), ovvero l'autenticazione del server (OID 1.3.6.1.5.5.7.3.1).</span><span class="sxs-lookup"><span data-stu-id="db12a-109">The certificate must contain the correct *Enhanced Key Usage* (EKU)—Server Authentication (OID 1.3.6.1.5.5.7.3.1).</span></span> <span data-ttu-id="db12a-110">Se il certificato non contiene questo EKU, il client termina la connessione.</span><span class="sxs-lookup"><span data-stu-id="db12a-110">If the certificate does not contain this EKU, the client ends the connection.</span></span>

-   <span data-ttu-id="db12a-111">Il nome di dominio completo (FQDN) del certificato deve corrispondere al server in cui è installato.</span><span class="sxs-lookup"><span data-stu-id="db12a-111">The certificate fully qualified domain name (FQDN) must match the server on which it is installed.</span></span> <span data-ttu-id="db12a-112">Ad esempio, se il client chiama `RTSPS://Myserver.mycompany.com/content/MyApp.sft` e il certificato **emesso per** il campo è impostato su `Server1.mycompany.com` , il client non si connette al server e la sessione termina.</span><span class="sxs-lookup"><span data-stu-id="db12a-112">For example, if the client is calling `RTSPS://Myserver.mycompany.com/content/MyApp.sft` and the certificate **Issued To** field is set to `Server1.mycompany.com`, the client will not connect to the server and the session ends.</span></span> <span data-ttu-id="db12a-113">L'errore viene segnalato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="db12a-113">The failure is reported to the user.</span></span>

    <span data-ttu-id="db12a-114">**Nota**  Se si usa App-V in un cluster di bilanciamento del carico di rete, è necessario configurare il certificato con i nomi alternativi oggetto (SANs) per supportare RTSPs.</span><span class="sxs-lookup"><span data-stu-id="db12a-114">**Note** If you are using App-V in a Network Load Balancing cluster, you must configure the certificate with Subject Alternate Names (SANs) to support RTSPS.</span></span> <span data-ttu-id="db12a-115">Per informazioni sulla configurazione dell'autorità di certificazione (CA) e sulla creazione di certificati con SANs, vedere <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="db12a-115">For information about configuring the certification authority (CA) and creating certificates with SANs, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

     

-   <span data-ttu-id="db12a-116">Il client e il server devono considerare attendibile la CA radice: la CA che rilascia il certificato al server App-V deve essere considerata attendibile dal client che si connette al server.</span><span class="sxs-lookup"><span data-stu-id="db12a-116">The client and the server need to trust the root CA—The CA issuing the certificate to the App-V server must by trusted by the client connecting to the server.</span></span> <span data-ttu-id="db12a-117">In caso contrario, il client termina la connessione.</span><span class="sxs-lookup"><span data-stu-id="db12a-117">If not, the client ends the connection.</span></span>

-   <span data-ttu-id="db12a-118">La chiave privata del certificato deve avere le autorizzazioni modificate per consentire all'account di servizio App-V di accedere al certificato.</span><span class="sxs-lookup"><span data-stu-id="db12a-118">The certificate’s private key must have permissions changed to allow the App-V Service account to access the certificate.</span></span> <span data-ttu-id="db12a-119">Per impostazione predefinita, App-V usa l'account del servizio di rete e, per impostazione predefinita, l'account del servizio di rete non ha l'autorizzazione per accedere alla chiave privata, impedendo connessioni sicure.</span><span class="sxs-lookup"><span data-stu-id="db12a-119">By default, App-V uses the Network Service account, and by default, the Network Service account does not have permission to access the private key, which will prevent secure connections.</span></span>

## <span data-ttu-id="db12a-120">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="db12a-120">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[<span data-ttu-id="db12a-121">Configurazione dei certificati per il supporto dello streaming sicuro</span><span class="sxs-lookup"><span data-stu-id="db12a-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)  
<span data-ttu-id="db12a-122">Fornisce informazioni su come ottenere, configurare e installare i certificati per supportare lo streaming sicuro.</span><span class="sxs-lookup"><span data-stu-id="db12a-122">Provides information about obtaining, configuring, and installing certificates to support secure streaming.</span></span>

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[<span data-ttu-id="db12a-123">Come modificare le autorizzazioni della chiave privata supportare Management Server o Streaming Server</span><span class="sxs-lookup"><span data-stu-id="db12a-123">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
<span data-ttu-id="db12a-124">Fornisce le procedure che è possibile usare per modificare le chiavi in Windows Server2003 e Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="db12a-124">Provides procedures you can use to modify keys in Windows Server2003 and Windows Server2008.</span></span>

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[<span data-ttu-id="db12a-125">Configurazione dei certificati per supportare App-V Management Server o Streaming Server</span><span class="sxs-lookup"><span data-stu-id="db12a-125">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
<span data-ttu-id="db12a-126">Fornisce informazioni sulla configurazione dei certificati per i server di gestione o di flusso di App-V, incluse informazioni sulla configurazione dei certificati per gli ambienti di bilanciamento del carico di rete.</span><span class="sxs-lookup"><span data-stu-id="db12a-126">Provides information about configuring certificates for the App-V Management or Streaming Servers, including information about configuring certificates for Network Load Balancing environments.</span></span>

 

 





