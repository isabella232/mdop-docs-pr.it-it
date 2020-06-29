---
title: Come configurare la sicurezza di Management Server dopo l'installazione
description: Come configurare la sicurezza di Management Server dopo l'installazione
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817936"
---
# <span data-ttu-id="e287d-103">Come configurare la sicurezza di Management Server dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="e287d-103">How to Configure Management Server Security Post-Installation</span></span>


<span data-ttu-id="e287d-104">Usare la console di gestione di App-V per aggiungere il certificato e configurare App-V Management Server per una maggiore sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e287d-104">Use the App-V Management Console to add the certificate and configure the App-V Management Server for enhanced security.</span></span> <span data-ttu-id="e287d-105">Per configurare la sicurezza post-installazione, è possibile usare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="e287d-105">You can use the following procedure to configure security post-installation.</span></span>

**<span data-ttu-id="e287d-106">Per configurare la sicurezza del server di gestione dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="e287d-106">To configure Management Server security post-installation</span></span>**

1.  <span data-ttu-id="e287d-107">Aprire la console di gestione di App-V e connettersi al **servizio di gestione** con i privilegi di amministratore di App-v.</span><span class="sxs-lookup"><span data-stu-id="e287d-107">Open the App-V Management Console, and connect to the **Management Service** with App-V administrator privileges.</span></span>

2.  <span data-ttu-id="e287d-108">Espandere il server, espandere **gruppi di server**e quindi selezionare il gruppo di server appropriato con cui è stato registrato il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="e287d-108">Expand the server, expand **Server Groups**, and then select the appropriate server group with which the Management Server was registered.</span></span>

3.  <span data-ttu-id="e287d-109">Fare clic con il pulsante destro del mouse sull'oggetto server di gestione e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="e287d-109">Right-click the Management Server object, and select **Properties**.</span></span>

4.  <span data-ttu-id="e287d-110">Nella scheda **porte** fare clic su **certificato server** e completare la procedura guidata per selezionare il certificato correttamente provisioning.</span><span class="sxs-lookup"><span data-stu-id="e287d-110">On the **Ports** tab, click **Server Certificate** and complete the wizard to select the properly provisioned certificate.</span></span>

    <span data-ttu-id="e287d-111">**Nota**  Se non vengono visualizzati certificati nella procedura guidata, non è stato effettuato il provisioning di un certificato o il certificato soddisfa i requisiti di App-V.</span><span class="sxs-lookup"><span data-stu-id="e287d-111">**Note** If no certificates are displayed in the wizard, a certificate has not been provisioned or the certificate does meet the requirements of App-V.</span></span>

     

5.  <span data-ttu-id="e287d-112">Fare clic su **Avanti** per passare alla pagina della **procedura guidata benvenuto in certificato** .</span><span class="sxs-lookup"><span data-stu-id="e287d-112">Click **Next** to continue on to the **Welcome To Certificate Wizard** page.</span></span>

6.  <span data-ttu-id="e287d-113">Selezionare il certificato corretto nella schermata **certificati disponibili** .</span><span class="sxs-lookup"><span data-stu-id="e287d-113">Select the correct certificate in the **Available Certificates** screen.</span></span>

7.  <span data-ttu-id="e287d-114">Fai clic su **Fine**.</span><span class="sxs-lookup"><span data-stu-id="e287d-114">Click **Finish**.</span></span>

8.  <span data-ttu-id="e287d-115">Dopo aver completato la procedura guidata, deselezionare **RTSP** come porta di ascolto disponibile.</span><span class="sxs-lookup"><span data-stu-id="e287d-115">After completing the wizard, clear **RTSP** as an available listening port.</span></span> <span data-ttu-id="e287d-116">In questo modo viene impedito l'effettuazione di connessioni su un canale di comunicazione non sicuro.</span><span class="sxs-lookup"><span data-stu-id="e287d-116">This prevents connections from being made over a non-secure communication channel.</span></span>

9.  <span data-ttu-id="e287d-117">Fare clic su **applica**e riavviare il servizio **Microsoft Virtual Application Server** .</span><span class="sxs-lookup"><span data-stu-id="e287d-117">Click **Apply**, and restart the **Microsoft Virtual Application Server** service.</span></span> <span data-ttu-id="e287d-118">Per eseguire questa attività, USA lo snap-in MMC del servizio.</span><span class="sxs-lookup"><span data-stu-id="e287d-118">Use the service’s MMC snap-in to accomplish this task.</span></span>

## <span data-ttu-id="e287d-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e287d-119">Related topics</span></span>


[<span data-ttu-id="e287d-120">Come configurare la sicurezza di Streaming Server dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="e287d-120">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)

[<span data-ttu-id="e287d-121">Risoluzione dei problemi di autorizzazione dei certificati</span><span class="sxs-lookup"><span data-stu-id="e287d-121">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





