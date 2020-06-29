---
title: Come configurare il firewall di Windows Server 2008 per App-V
description: Come configurare il firewall di Windows Server 2008 per App-V
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817716"
---
# <span data-ttu-id="f07a1-103">Come configurare il firewall di Windows Server 2008 per App-V</span><span class="sxs-lookup"><span data-stu-id="f07a1-103">How to Configure Windows Server 2008 Firewall for App-V</span></span>


<span data-ttu-id="f07a1-104">Con l'introduzione di Windows Server2008, il firewall e i componenti IPsec sono Stati Uniti in un unico servizio e le funzionalità di questo servizio sono state migliorate.</span><span class="sxs-lookup"><span data-stu-id="f07a1-104">With the introduction of Windows Server2008, the firewall and IPsec components were merged into one service, and the capabilities of this service were enhanced.</span></span> <span data-ttu-id="f07a1-105">Il nuovo servizio firewall supporta il controllo con stato in arrivo e in uscita.</span><span class="sxs-lookup"><span data-stu-id="f07a1-105">The new firewall service supports incoming and outgoing stateful inspection.</span></span> <span data-ttu-id="f07a1-106">È inoltre possibile configurare regole firewall e criteri IPsec specifici tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f07a1-106">Also, you can configure specific firewall rules and IPsec policies through group policies.</span></span> <span data-ttu-id="f07a1-107">Per altre informazioni su Windows Firewall in Windows Server2008, vedere <https://go.microsoft.com/fwlink/?LinkId=151980> .</span><span class="sxs-lookup"><span data-stu-id="f07a1-107">For additional information about the Windows firewall in Windows Server2008, see <https://go.microsoft.com/fwlink/?LinkId=151980>.</span></span>

<span data-ttu-id="f07a1-108">La procedura seguente non include l'aggiunta di un'eccezione per la pubblicazione di ICO e OSD tramite SMB o HTTP/HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f07a1-108">The following procedure does not include adding an exception for ICO and OSD publishing through SMB or HTTP/HTTPS.</span></span> <span data-ttu-id="f07a1-109">Tali eccezioni vengono aggiunte automaticamente in base al profilo di rete e ai ruoli installati nel firewall di Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f07a1-109">Those exceptions are automatically added based on the network profile and roles installed on the Windows Server 2008 firewall.</span></span>

<span data-ttu-id="f07a1-110">**Nota**  Se il server di gestione è configurato per l'uso di RTSP, ripetere questa procedura per aggiungere il `sghwsvr.exe` programma come eccezione.</span><span class="sxs-lookup"><span data-stu-id="f07a1-110">**Note** If the Management Server is configured to use RTSP, repeat this procedure to add the `sghwsvr.exe` program as an exception.</span></span>

<span data-ttu-id="f07a1-111">App-V Streaming Server richiede l'eccezione del programma `sglwdsptr.exe` per la comunicazione RTSPS.</span><span class="sxs-lookup"><span data-stu-id="f07a1-111">The App-V Streaming Server requires the program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="f07a1-112">Un App-V streaming server che usa RTSP per comunicare richiede anche un'eccezione per il programma `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="f07a1-112">An App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

 

**<span data-ttu-id="f07a1-113">Per configurare il firewall di Windows Server2008 per App-V</span><span class="sxs-lookup"><span data-stu-id="f07a1-113">To configure Windows Server2008 firewall for App-V</span></span>**

1.  <span data-ttu-id="f07a1-114">Aprire **Windows Firewall con Advanced Security** Management Console tramite il pannello di controllo oppure digitando `wf.msc` la riga Esegui.</span><span class="sxs-lookup"><span data-stu-id="f07a1-114">Open the **Windows Firewall with Advanced Security** management console through the Control Panel or by typing `wf.msc` on the Run line.</span></span>

2.  <span data-ttu-id="f07a1-115">Creare una nuova regola in entrata e selezionare **programma**.</span><span class="sxs-lookup"><span data-stu-id="f07a1-115">Create a new inbound rule, and select **Program**.</span></span>

3.  <span data-ttu-id="f07a1-116">Selezionare il percorso del programma e passare a `sghwdsptr.exe` , che si trova per impostazione predefinita `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="f07a1-116">Select the program path, and browse to `sghwdsptr.exe`, which is located by default at `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

4.  <span data-ttu-id="f07a1-117">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f07a1-117">Click **Next**.</span></span>

5.  <span data-ttu-id="f07a1-118">Nella pagina **azione** selezionare **Consenti la connessione**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f07a1-118">On the **Action** page, select **Allow the connection**, and then click **Next**.</span></span>

6.  <span data-ttu-id="f07a1-119">Selezionare i **profili** appropriati da applicare alla regola in ingresso.</span><span class="sxs-lookup"><span data-stu-id="f07a1-119">Select the appropriate **Profiles** to apply to the inbound rule.</span></span>

7.  <span data-ttu-id="f07a1-120">Specificare un nome e una descrizione per la regola e fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="f07a1-120">Provide a name and description for the rule, and click **Finish**.</span></span>

## <span data-ttu-id="f07a1-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f07a1-121">Related topics</span></span>


[<span data-ttu-id="f07a1-122">Come configurare il firewall di Windows Server 2003 per App-V</span><span class="sxs-lookup"><span data-stu-id="f07a1-122">How to Configure Windows Server 2003 Firewall for App-V</span></span>](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





