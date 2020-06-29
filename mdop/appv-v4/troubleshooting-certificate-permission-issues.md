---
title: Risoluzione dei problemi di autorizzazione dei certificati
description: Risoluzione dei problemi di autorizzazione dei certificati
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815206"
---
# <span data-ttu-id="b6a47-103">Risoluzione dei problemi di autorizzazione dei certificati</span><span class="sxs-lookup"><span data-stu-id="b6a47-103">Troubleshooting Certificate Permission Issues</span></span>


<span data-ttu-id="b6a47-104">Dopo l'installazione di App-V 4.5, se la chiave privata non è stata configurata con l'ACL appropriato per il servizio di rete, viene registrato un evento nel log eventi di NT e viene inserita una voce nel `Sft-server.log` file.</span><span class="sxs-lookup"><span data-stu-id="b6a47-104">After the installation of App-V4.5, if the private key has not been configured with the proper ACL for the Network Service, an event is logged in the NT Event Log and an entry is placed in the `Sft-server.log` file.</span></span>

## <span data-ttu-id="b6a47-105">Messaggi di errore</span><span class="sxs-lookup"><span data-stu-id="b6a47-105">Error Messages</span></span>


### <span data-ttu-id="b6a47-106">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="b6a47-106">Windows Server2003</span></span>

<span data-ttu-id="b6a47-107">ID evento 36870: si è verificato un errore irreversibile durante il tentativo di accesso alla chiave privata delle credenziali del server SSL.</span><span class="sxs-lookup"><span data-stu-id="b6a47-107">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="b6a47-108">Il codice di errore restituito dal modulo crittografico è 0x80090016.</span><span class="sxs-lookup"><span data-stu-id="b6a47-108">The error code returned from the cryptographic module is 0x80090016.</span></span>

### <span data-ttu-id="b6a47-109">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="b6a47-109">Windows Server2008</span></span>

<span data-ttu-id="b6a47-110">ID evento 36870: si è verificato un errore irreversibile durante il tentativo di accesso alla chiave privata delle credenziali del server SSL.</span><span class="sxs-lookup"><span data-stu-id="b6a47-110">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="b6a47-111">Il codice di errore restituito dal modulo crittografico è 0x8009030d.</span><span class="sxs-lookup"><span data-stu-id="b6a47-111">The error code returned from the cryptographic module is 0x8009030d.</span></span>

## <span data-ttu-id="b6a47-112">SFT-server. log</span><span class="sxs-lookup"><span data-stu-id="b6a47-112">Sft-server.log</span></span>


<span data-ttu-id="b6a47-113">L'errore seguente viene inserito nel `sft-server.log` file che si trova nella `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` Directory:</span><span class="sxs-lookup"><span data-stu-id="b6a47-113">The following error is placed in the `sft-server.log` file located in the `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` directory:</span></span>

<span data-ttu-id="b6a47-114">Non è stato possibile caricare il certificato.</span><span class="sxs-lookup"><span data-stu-id="b6a47-114">Certificate could not be loaded.</span></span> <span data-ttu-id="b6a47-115">Codice di errore \ [-2146893043 \].</span><span class="sxs-lookup"><span data-stu-id="b6a47-115">Error code \[-2146893043\].</span></span> <span data-ttu-id="b6a47-116">Verificare che l'account del servizio di rete disponga dell'accesso corretto al certificato e al file della chiave privata corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b6a47-116">Make sure that the Network Service account has proper access to the certificate and its corresponding private key file.</span></span>

 

 





