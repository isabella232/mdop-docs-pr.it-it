---
title: Come configurare la sicurezza di Streaming Server dopo l'installazione
description: Come configurare la sicurezza di Streaming Server dopo l'installazione
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817905"
---
# <span data-ttu-id="d4e17-103">Come configurare la sicurezza di Streaming Server dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="d4e17-103">How to Configure Streaming Server Security Post-Installation</span></span>


<span data-ttu-id="d4e17-104">Configurare App-V Streaming Server per una maggiore sicurezza tramite il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d4e17-104">Configure the App-V Streaming Server for enhanced security through the registry.</span></span> <span data-ttu-id="d4e17-105">Come per l'App-V Management Server, un certificato deve essere correttamente provisioning con l'identificatore EKU corretto per l'autenticazione del server prima di completare la procedura di post-installazione seguente.</span><span class="sxs-lookup"><span data-stu-id="d4e17-105">As with the App-V Management Server, a certificate must be correctly provisioned with the correct EKU identifier for Server Authentication before you complete the following post-installation procedure.</span></span>

**<span data-ttu-id="d4e17-106">Per configurare la post-installazione di Streaming Server Security</span><span class="sxs-lookup"><span data-stu-id="d4e17-106">To configure Streaming Server security post-installation</span></span>**

1.  <span data-ttu-id="d4e17-107">Creare una console MMC, aggiungere lo snap-in **certificati** e selezionare **archivio certificati computer locale**.</span><span class="sxs-lookup"><span data-stu-id="d4e17-107">Create an MMC, add the **Certificates** snap-in, and select **Local Machine certificate store**.</span></span>

2.  <span data-ttu-id="d4e17-108">Aprire i certificati **personali** per il computer e aprire il provisioning del certificato per App-V.</span><span class="sxs-lookup"><span data-stu-id="d4e17-108">Open the **Personal** certificates for the computer, and open the certificate provisioned for App-V.</span></span>

3.  <span data-ttu-id="d4e17-109">Nella scheda **Dettagli** scorrere verso il basso fino all'identificazione personale e copiare l'hash nel riquadro dei dettagli.</span><span class="sxs-lookup"><span data-stu-id="d4e17-109">On the **Details** tab, scroll down to the thumbprint and copy the hash in the details pane.</span></span>

4.  <span data-ttu-id="d4e17-110">Aprire l'editor del registro di sistema e passare a `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` .</span><span class="sxs-lookup"><span data-stu-id="d4e17-110">Open the registry editor, and navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server`.</span></span>

5.  <span data-ttu-id="d4e17-111">Modificare il `X509CertHash` valore, incollare l'hash delle identificazioni personali nel campo valore e rimuovere tutti gli spazi.</span><span class="sxs-lookup"><span data-stu-id="d4e17-111">Edit the `X509CertHash` value, paste the thumbprint hash in the value field, and remove all spaces.</span></span> <span data-ttu-id="d4e17-112">Fare clic su **OK** per accettare la modifica.</span><span class="sxs-lookup"><span data-stu-id="d4e17-112">Click **OK** to accept the edit.</span></span>

6.  <span data-ttu-id="d4e17-113">Nell'editor del registro di sistema passare a `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` .</span><span class="sxs-lookup"><span data-stu-id="d4e17-113">In the registry editor, navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts`.</span></span>

7.  <span data-ttu-id="d4e17-114">Creare un nuovo valore **DWORD** denominato "322" e quindi immettere il valore decimale come 322 o il valore esadecimale come 142.</span><span class="sxs-lookup"><span data-stu-id="d4e17-114">Create a new **DWORD** value named "322," and then enter the decimal value as 322 or the hexadecimal value as 142.</span></span>

8.  <span data-ttu-id="d4e17-115">Riavviare il servizio di streaming.</span><span class="sxs-lookup"><span data-stu-id="d4e17-115">Restart the streaming service.</span></span>

## <span data-ttu-id="d4e17-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d4e17-116">Related topics</span></span>


[<span data-ttu-id="d4e17-117">Come configurare la sicurezza di Management Server dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="d4e17-117">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)

[<span data-ttu-id="d4e17-118">Risoluzione dei problemi di autorizzazione dei certificati</span><span class="sxs-lookup"><span data-stu-id="d4e17-118">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





