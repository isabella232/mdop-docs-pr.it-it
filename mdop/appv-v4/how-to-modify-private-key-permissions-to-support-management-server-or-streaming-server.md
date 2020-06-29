---
title: Come modificare le autorizzazioni della chiave privata supportare Management Server o Streaming Server
description: Come modificare le autorizzazioni della chiave privata supportare Management Server o Streaming Server
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817026"
---
# <span data-ttu-id="42586-103">Come modificare le autorizzazioni della chiave privata supportare Management Server o Streaming Server</span><span class="sxs-lookup"><span data-stu-id="42586-103">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>


<span data-ttu-id="42586-104">Per supportare un'installazione di App-V più sicura, è possibile usare le procedure seguenti per modificare le chiavi private in Windows Server2003 o Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="42586-104">To support a more secure App-V installation, you can use the following procedures to modify private keys in either Windows Server2003 or Windows Server2008.</span></span> <span data-ttu-id="42586-105">Per modificare le autorizzazioni della chiave privata, è possibile usare lo strumento Windows Server2003 Resource Kit `WinHttpCertCfg.exe` .</span><span class="sxs-lookup"><span data-stu-id="42586-105">To modify the permissions of the private key, you can use the Windows Server2003 Resource Kit tool `WinHttpCertCfg.exe`.</span></span>

<span data-ttu-id="42586-106">Per Windows Server2003, la procedura richiede che un certificato che soddisfi i prerequisiti elencati in questo documento sia installato nel computer o nei computer in cui si vuole installare App-V Management o streaming server.</span><span class="sxs-lookup"><span data-stu-id="42586-106">For Windows Server2003, the procedure requires that a certificate that meets the prerequisites listed in this document is installed on the computer or computers on which you will install the App-V Management or Streaming Server.</span></span> <span data-ttu-id="42586-107">Altre informazioni sull'uso dello `WinHttpCertCfg.exe` strumento sono disponibili all'indirizzo <https://go.microsoft.com/fwlink/?LinkId=151981> .</span><span class="sxs-lookup"><span data-stu-id="42586-107">Additional information about using the `WinHttpCertCfg.exe` tool is available at <https://go.microsoft.com/fwlink/?LinkId=151981>.</span></span>

<span data-ttu-id="42586-108">In Windows Server2008, il processo di modifica degli ACL della chiave privata è molto più semplice.</span><span class="sxs-lookup"><span data-stu-id="42586-108">In Windows Server2008, the process of changing the ACLs on the private key is much simpler.</span></span> <span data-ttu-id="42586-109">L'interfaccia utente del certificato può essere usata per gestire le autorizzazioni di chiave privata.</span><span class="sxs-lookup"><span data-stu-id="42586-109">The certificate’s user interface can be used to manage private key permissions.</span></span>

<span data-ttu-id="42586-110">**Nota**  Il contesto di sicurezza predefinito è servizio di rete; Tuttavia, è possibile usare un account di dominio.</span><span class="sxs-lookup"><span data-stu-id="42586-110">**Note** The default security context is Network Service; however, a domain account can be used instead.</span></span>

 

**<span data-ttu-id="42586-111">Per gestire le chiavi private in Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="42586-111">To manage private keys in Windows Server2003</span></span>**

1.  <span data-ttu-id="42586-112">Nel computer che diventerà App-V Management o streaming server digitare il comando seguente in un prompt dei comandi per elencare le autorizzazioni correnti assegnate a un certificato specifico:</span><span class="sxs-lookup"><span data-stu-id="42586-112">On the computer that will become the App-V Management or Streaming Server, type the following command in a command prompt to list the current permissions assigned to a specific certificate:</span></span>

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  <span data-ttu-id="42586-113">Se necessario, modificare le autorizzazioni del certificato per consentire l'accesso in lettura al contesto di sicurezza che verrà usato per la gestione o il servizio di flusso:</span><span class="sxs-lookup"><span data-stu-id="42586-113">If necessary, modify the permissions of the certificate to provide read access to the security context that will be used for Management or Streaming Service:</span></span>

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  <span data-ttu-id="42586-114">Verificare che il contesto di sicurezza sia stato aggiunto correttamente elencando le autorizzazioni per il certificato:</span><span class="sxs-lookup"><span data-stu-id="42586-114">Verify that the security context was properly added by listing the permissions on the certificate:</span></span>

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**<span data-ttu-id="42586-115">Per gestire le chiavi private in Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="42586-115">To manage private keys in Windows Server2008</span></span>**

1.  <span data-ttu-id="42586-116">Creare una Microsoft Management Console (MMC) con lo snap-in *certificati* destinato all'archivio certificati del *computer locale* .</span><span class="sxs-lookup"><span data-stu-id="42586-116">Create a Microsoft Management Console (MMC) with the *Certificates* snap-in that targets the *Local Machine* certificate store.</span></span>

2.  <span data-ttu-id="42586-117">Espandere la console MMC e selezionare **Gestisci chiavi private**.</span><span class="sxs-lookup"><span data-stu-id="42586-117">Expand the MMC and select **Manage Private Keys**.</span></span>

3.  <span data-ttu-id="42586-118">Nella scheda **sicurezza** aggiungere l'account del **servizio di rete** con l'accesso in **lettura** .</span><span class="sxs-lookup"><span data-stu-id="42586-118">On the **Security** tab, add the **Network Service** account with **Read** access.</span></span>

## <span data-ttu-id="42586-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42586-119">Related topics</span></span>


[<span data-ttu-id="42586-120">Configurazione dei certificati per supportare App-V Management Server o Streaming Server</span><span class="sxs-lookup"><span data-stu-id="42586-120">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[<span data-ttu-id="42586-121">Configurazione dei certificati per il supporto dello streaming sicuro</span><span class="sxs-lookup"><span data-stu-id="42586-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

 

 





