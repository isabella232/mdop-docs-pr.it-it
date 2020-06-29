---
title: Configurazione dei certificati per il supporto dello streaming sicuro
description: Configurazione dei certificati per il supporto dello streaming sicuro
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821895"
---
# <span data-ttu-id="7fda1-103">Configurazione dei certificati per il supporto dello streaming sicuro</span><span class="sxs-lookup"><span data-stu-id="7fda1-103">Configuring Certificates to Support Secure Streaming</span></span>


<span data-ttu-id="7fda1-104">Per impostazione predefinita, il servizio App-V viene eseguito con l'account del servizio di rete.</span><span class="sxs-lookup"><span data-stu-id="7fda1-104">By default, the App-V service runs under the Network Service account.</span></span> <span data-ttu-id="7fda1-105">È tuttavia possibile creare un account del servizio in servizi di dominio Active Directory e sostituire l'account del servizio di rete con l'account di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7fda1-105">However, you can create a service account in Active Directory Domain Services and replace the Network Service account with the Active Directory Domain account.</span></span>

<span data-ttu-id="7fda1-106">Il contesto di sicurezza in cui viene eseguito il servizio è importante per la configurazione di comunicazioni sicure avanzate.</span><span class="sxs-lookup"><span data-stu-id="7fda1-106">The security context under which the service runs is important for configuring enhanced secure communications.</span></span> <span data-ttu-id="7fda1-107">Questo contesto di sicurezza deve avere le autorizzazioni di lettura per la chiave privata del certificato.</span><span class="sxs-lookup"><span data-stu-id="7fda1-107">This security context must have read permissions for the certificate private key.</span></span> <span data-ttu-id="7fda1-108">Quando viene generata una *richiesta di firma del certificato* PKCS \ #10 (CSR) per il server App-V, viene chiamato il provider del *servizio crittografico* di Windows e viene generata una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="7fda1-108">When a PKCS\#10 *Certificate Signing Request* (CSR) is generated for the App-V server, the Windows *Cryptographic Service Provider* is called and a private key is generated.</span></span> <span data-ttu-id="7fda1-109">La chiave privata è protetta con le autorizzazioni concesse solo agli account di sistema e amministratore.</span><span class="sxs-lookup"><span data-stu-id="7fda1-109">The private key is secured with permissions given to the System and Administrator accounts only.</span></span>

<span data-ttu-id="7fda1-110">È necessario modificare gli elenchi di controllo di accesso (ACL) sulla chiave privata per consentire all'App-V Management o al server di streaming di accedere alla chiave privata necessaria per la corretta comunicazione protetta TLS.</span><span class="sxs-lookup"><span data-stu-id="7fda1-110">You must modify the access control lists (ACLs) on the private key to let the App-V Management or Streaming Server access the private key required for successful TLS secured communication.</span></span>

## <span data-ttu-id="7fda1-111">Recupero e installazione di un certificato</span><span class="sxs-lookup"><span data-stu-id="7fda1-111">Obtaining and Installing a Certificate</span></span>


<span data-ttu-id="7fda1-112">Gli scenari per ottenere e installare un certificato per App-V sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7fda1-112">The scenarios for obtaining and installing a certificate for App-V are as follows:</span></span>

-   <span data-ttu-id="7fda1-113">Infrastruttura a chiave pubblica interna (PKI).</span><span class="sxs-lookup"><span data-stu-id="7fda1-113">Internal public key infrastructure (PKI).</span></span>

-   <span data-ttu-id="7fda1-114">Autorità di certificazione (CA) che rilascia certificati di terze parti.</span><span class="sxs-lookup"><span data-stu-id="7fda1-114">Third-party certificate issuing certification authority (CA).</span></span>

    <span data-ttu-id="7fda1-115">**Nota**  Se è necessario ottenere un certificato da una CA di terze parti, seguire la documentazione disponibile nel sito Web della CA.</span><span class="sxs-lookup"><span data-stu-id="7fda1-115">**Note** If you need to obtain a certificate from a third-party CA, follow the documentation available on that CA’s Web site.</span></span>

     

<span data-ttu-id="7fda1-116">Se è stata distribuita un'infrastruttura PKI, consultare gli amministratori della PKI per acquisire un certificato conforme ai requisiti descritti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="7fda1-116">If a PKI infrastructure has been deployed, consult with the PKI administrators to acquire a certificate that complies with the requirements described in this topic.</span></span> <span data-ttu-id="7fda1-117">Se un'infrastruttura PKI non è disponibile, usare un'autorità di certificazione di terze parti per ottenere un certificato valido.</span><span class="sxs-lookup"><span data-stu-id="7fda1-117">If a PKI infrastructure is not available, use a third-party CA to obtain a valid certificate.</span></span>

<span data-ttu-id="7fda1-118">Per informazioni dettagliate su come ottenere e installare un certificato, vedere <https://go.microsoft.com/fwlink/?LinkId=151969> .</span><span class="sxs-lookup"><span data-stu-id="7fda1-118">For step-by-step guidance for obtaining and installing a certificate, see <https://go.microsoft.com/fwlink/?LinkId=151969>.</span></span>

## <span data-ttu-id="7fda1-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fda1-119">Related topics</span></span>


<span data-ttu-id="7fda1-120">Configurazione dei certificati per il supporto dello streaming sicuro [come modificare le autorizzazioni di chiave privata per supportare server di gestione o streaming server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span><span class="sxs-lookup"><span data-stu-id="7fda1-120">Configuring Certificates to Support Secure Streaming [How to Modify Private Key Permissions to Support Management Server or Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span></span>

 

 





