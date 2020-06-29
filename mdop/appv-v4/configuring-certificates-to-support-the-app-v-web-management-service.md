---
title: Configurazione dei certificati per supportare il Servizio gestione Web di App-V
description: Configurazione dei certificati per supportare il Servizio gestione Web di App-V
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821886"
---
# <span data-ttu-id="c3426-103">Configurazione dei certificati per supportare il Servizio gestione Web di App-V</span><span class="sxs-lookup"><span data-stu-id="c3426-103">Configuring Certificates to Support the App-V Web Management Service</span></span>


<span data-ttu-id="c3426-104">Il servizio di gestione Web App-V deve essere configurato per supportare le connessioni basate su SSL per proteggere la comunicazione.</span><span class="sxs-lookup"><span data-stu-id="c3426-104">The App-V Web Management Service must be configured to support SSL-based connections to help secure the communication.</span></span> <span data-ttu-id="c3426-105">Questo processo richiede che il server Web o il computer in cui è installato il servizio di gestione disponga di un certificato rilasciato al servizio o al computer.</span><span class="sxs-lookup"><span data-stu-id="c3426-105">This process requires that the Web server or computer on which the Management Service is installed has a certificate issued to the service or computer.</span></span>

<span data-ttu-id="c3426-106">Gli scenari seguenti illustrano come ottenere un certificato a questo scopo:</span><span class="sxs-lookup"><span data-stu-id="c3426-106">The following scenarios illustrate how to obtain a certificate for this purpose:</span></span>

1.  <span data-ttu-id="c3426-107">Nell'infrastruttura aziendale è già presente un'infrastruttura a chiave pubblica (PKI) che emette automaticamente i certificati per i computer.</span><span class="sxs-lookup"><span data-stu-id="c3426-107">The company infrastructure already has a public key infrastructure (PKI) in place that automatically issues certificates to computers.</span></span>

2.  <span data-ttu-id="c3426-108">L'infrastruttura aziendale ha già una PKI in posizione, anche se non rilascia automaticamente certificati ai computer.</span><span class="sxs-lookup"><span data-stu-id="c3426-108">The company infrastructure already has a PKI in place, although it does not automatically issue certificates to computers.</span></span>

3.  <span data-ttu-id="c3426-109">L'infrastruttura aziendale non ha una PKI in posizione.</span><span class="sxs-lookup"><span data-stu-id="c3426-109">The company infrastructure has no PKI in place.</span></span>

<span data-ttu-id="c3426-110">In ognuno degli scenari precedenti, il metodo per ottenere un certificato è diverso, ma il risultato finale è lo stesso.</span><span class="sxs-lookup"><span data-stu-id="c3426-110">In each of the preceding scenarios, the method for obtaining a certificate is different, but the end result is the same.</span></span> <span data-ttu-id="c3426-111">L'amministratore deve assegnare un certificato al sito Web predefinito di IIS e configurare il servizio di gestione Web App-V per richiedere comunicazioni sicure.</span><span class="sxs-lookup"><span data-stu-id="c3426-111">The administrator must assign a certificate to the IIS Default Web Site and configure the App-V Web Management Service to require secure communications.</span></span>

<span data-ttu-id="c3426-112">**Importante**  Il nome del certificato deve corrispondere al nome del server.</span><span class="sxs-lookup"><span data-stu-id="c3426-112">**Important** The name of the certificate must match the name of the server.</span></span> <span data-ttu-id="c3426-113">È consigliabile usare nomi di dominio completi (FQDN) per il nome comune del certificato.</span><span class="sxs-lookup"><span data-stu-id="c3426-113">It is a best practice to use fully qualified domain names (FQDNs) for the common name of the certificate.</span></span>

 

<span data-ttu-id="c3426-114">App-V può usare i server IIS per supportare diverse configurazioni di infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="c3426-114">App-V can use IIS servers to support different infrastructure configurations.</span></span> <span data-ttu-id="c3426-115">Per altre informazioni sulla configurazione dei server IIS per il supporto di HTTPS, vedere <https://go.microsoft.com/fwlink/?LinkId=151972> .</span><span class="sxs-lookup"><span data-stu-id="c3426-115">For more information about configuring IIS servers to support HTTPS, see <https://go.microsoft.com/fwlink/?LinkId=151972>.</span></span>

## <span data-ttu-id="c3426-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3426-116">Related topics</span></span>


[<span data-ttu-id="c3426-117">Come installare e configurare App-V Management Console per un ambiente più sicuro</span><span class="sxs-lookup"><span data-stu-id="c3426-117">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





