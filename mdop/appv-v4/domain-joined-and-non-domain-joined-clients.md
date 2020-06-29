---
title: Client aggiunti e non aggiunti a un dominio
description: Client aggiunti e non aggiunti a un dominio
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821635"
---
# <span data-ttu-id="e6898-103">Client aggiunti e non aggiunti a un dominio</span><span class="sxs-lookup"><span data-stu-id="e6898-103">Domain-Joined and Non-Domain-Joined Clients</span></span>


<span data-ttu-id="e6898-104">Il client Desktop App-V può essere configurato per consentire la connessione a una rete indipendentemente dal fatto che il client sia collegato al dominio o non sia stato aggiunto un dominio.</span><span class="sxs-lookup"><span data-stu-id="e6898-104">The App-V Desktop Client can be configured to allow connection to a network regardless of whether the client is domain joined or non-domain joined.</span></span>

## <span data-ttu-id="e6898-105">Client appartenenti a un dominio</span><span class="sxs-lookup"><span data-stu-id="e6898-105">Domain-Joined Clients</span></span>


<span data-ttu-id="e6898-106">I client che fanno parte di un dominio, ma all'esterno della rete interna, possono comunicare con l'infrastruttura App-V usando una connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="e6898-106">Clients that are domain joined, but outside the internal network, can communicate with the App-V infrastructure by using a VPN connection.</span></span> <span data-ttu-id="e6898-107">Quando si vuole consentire agli utenti di uscire dalla rete interna ma di comunicare ancora in un'infrastruttura App-V, l'ambiente richiede pochissima configurazione.</span><span class="sxs-lookup"><span data-stu-id="e6898-107">When you want to provide users the ability to leave the internal network but still communicate in an App-V infrastructure, your environment requires very little setup.</span></span> <span data-ttu-id="e6898-108">Poiché gli utenti fanno già parte del dominio, devi semplicemente assicurarti che le credenziali memorizzate nella cache siano supportate nel client.</span><span class="sxs-lookup"><span data-stu-id="e6898-108">Because the users are already part of the domain, you simply need to ensure that Cached Credentials are supported on the client.</span></span> <span data-ttu-id="e6898-109">Questa è la configurazione predefinita e tutte le modifiche apportate a questa impostazione possono essere eseguite da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="e6898-109">This is the default configuration, and any changes to this setting can be accomplished from Group Policies.</span></span>

<span data-ttu-id="e6898-110">Come accennato nella Guida alle procedure consigliate di App-V Security, l'utente tenterà di inviare il proprio ticket utente all'infrastruttura App-V per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="e6898-110">As mentioned in the App-V Security Best Practices Guide, the user will attempt to send their user ticket to the App-V infrastructure for authentication.</span></span> <span data-ttu-id="e6898-111">Se il ticket è scaduto, verrà ripristinato l'uso di NTLM e le credenziali memorizzate nella cache nel computer.</span><span class="sxs-lookup"><span data-stu-id="e6898-111">If the ticket is expired, it will revert to using NTLM and the cached credentials on the computer.</span></span> <span data-ttu-id="e6898-112">Per consentire il roaming, gli amministratori devono garantire che il server di pubblicazione a cui si accede internamente sia disponibile con lo stesso nome esternamente affinché i nomi vengano risolti in modo corretto.</span><span class="sxs-lookup"><span data-stu-id="e6898-112">To allow roaming, administrators must ensure that the publishing server being accessed internally is available at the same name externally for the names to resolve properly.</span></span>

## <span data-ttu-id="e6898-113">Client non appartenenti a un dominio</span><span class="sxs-lookup"><span data-stu-id="e6898-113">Non-Domain-Joined Clients</span></span>


<span data-ttu-id="e6898-114">I client che non sono collegati a un dominio, ma devono comunicare nell'infrastruttura di App-V, devono essere configurati in modo che l'autenticazione per l'infrastruttura App-V abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e6898-114">Clients that are non-domain joined but need to communicate in the App-V infrastructure must be configured to ensure that authentication to the App-V infrastructure is successful.</span></span> <span data-ttu-id="e6898-115">Il client desktop di App-V non consente la richiesta di conferma per il processo di aggiornamento della pubblicazione, quindi il client deve essere configurato per presentare le credenziali appropriate per l'App-V Management Server.</span><span class="sxs-lookup"><span data-stu-id="e6898-115">The App-V Desktop Client does not permit prompting for the publishing refresh process, so the client must be configured to present the proper credentials to the App-V Management Server.</span></span>

<span data-ttu-id="e6898-116">Il server di pubblicazione, configurato per l'aggiornamento della pubblicazione dal client non appartenente al dominio, richiede che il nome esterno che l'accesso ai client sia configurato come nome comune o un nome alternativo soggetto (SAN) nel certificato del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="e6898-116">The publishing server, which is configured for publishing refresh from the non-domain joined client, requires that the external name that clients access is configured as the common name or a subject alternate name (SAN) on the publishing server’s certificate.</span></span>

## <span data-ttu-id="e6898-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6898-117">Related topics</span></span>


[<span data-ttu-id="e6898-118">Come assegnare le credenziali appropriate per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6898-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

[<span data-ttu-id="e6898-119">Come assegnare le credenziali appropriate per Windows XP</span><span class="sxs-lookup"><span data-stu-id="e6898-119">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





