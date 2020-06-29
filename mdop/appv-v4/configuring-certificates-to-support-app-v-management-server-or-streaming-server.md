---
title: Configurazione dei certificati per supportare App-V Management Server o Streaming Server
description: Configurazione dei certificati per supportare App-V Management Server o Streaming Server
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821896"
---
# <span data-ttu-id="6a466-103">Configurazione dei certificati per supportare App-V Management Server o Streaming Server</span><span class="sxs-lookup"><span data-stu-id="6a466-103">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>


<span data-ttu-id="6a466-104">Dopo aver completato il processo di provisioning dei certificati e aver modificato le autorizzazioni per la chiave privata per supportare l'installazione di App-V, è possibile avviare la configurazione del server di gestione o del server di flusso.</span><span class="sxs-lookup"><span data-stu-id="6a466-104">After you complete the certificate provisioning process and change the private key permissions to support the App-V installation, you can launch the setup of the Management Server or the Streaming Server.</span></span> <span data-ttu-id="6a466-105">Durante l'installazione, se viene eseguito il provisioning di un certificato prima di eseguire il programma di installazione, la procedura guidata Visualizza il certificato nella schermata **modalità di sicurezza della connessione** e, per impostazione predefinita, la casella di controllo **Usa sicurezza avanzata** è selezionata.</span><span class="sxs-lookup"><span data-stu-id="6a466-105">During setup, if a certificate is provisioned before running the setup program, the wizard displays the certificate in the **Connection Security Mode** screen and, by default, the **Use enhanced security** check box is selected.</span></span>

<span data-ttu-id="6a466-106">**Nota**  Selezionare il certificato configurato per App-V se sono presenti più certificati per il server.</span><span class="sxs-lookup"><span data-stu-id="6a466-106">**Note** Select the certificate that was configured for App-V if there is more than one certificate provisioned for this server.</span></span>

 

<span data-ttu-id="6a466-107">**Importante**  Quando si esegue l'aggiornamento dalla versione 4,2 alla versione 4,5, il programma di installazione ha un'opzione per l' **uso della sicurezza avanzata**; Tuttavia, se si seleziona questa opzione, il flusso non verrà disabilitato tramite RTSP.</span><span class="sxs-lookup"><span data-stu-id="6a466-107">**Important** When upgrading from version 4.2 to version 4.5, the setup has an option for **Use enhanced security**; however, selecting this option will not disable streaming over RTSP.</span></span> <span data-ttu-id="6a466-108">È necessario usare la console di gestione per disabilitare RTSP dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="6a466-108">You must use the Management Console to disable RTSP after installation.</span></span>

 

<span data-ttu-id="6a466-109">Selezionare la porta TCP che il servizio userà per le comunicazioni client.</span><span class="sxs-lookup"><span data-stu-id="6a466-109">Select the TCP port that the service will use for client communications.</span></span> <span data-ttu-id="6a466-110">La porta predefinita è TCP 322; è tuttavia possibile cambiare la porta in una porta personalizzata per l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="6a466-110">The default port is TCP 322; however, you can change the port to a custom port for your environment.</span></span>

<span data-ttu-id="6a466-111">I passaggi rimanenti della procedura guidata sono gli stessi di quelli che si stavano distribuendo in un'app-V Management o in un server di streaming senza usare la funzionalità di **sicurezza avanzata** .</span><span class="sxs-lookup"><span data-stu-id="6a466-111">The remaining steps of the wizard are the same as if you were deploying an App-V Management or Streaming Server without using the **Enhanced security** feature.</span></span>

## <span data-ttu-id="6a466-112">Configurazione di certificati per gli ambienti NLB</span><span class="sxs-lookup"><span data-stu-id="6a466-112">Configuring Certificates for NLB Environments</span></span>


<span data-ttu-id="6a466-113">Per supportare le grandi aziende, spesso il server di gestione viene inserito in un cluster di bilanciamento del carico di rete (NLB) per supportare il numero elevato di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6a466-113">To support large enterprises, often the Management Server is placed into a Network Load Balancing (NLB) cluster to support the large number of connections.</span></span> <span data-ttu-id="6a466-114">In questo articolo sono necessari almeno due server di gestione che sembrano essere un singolo server di gestione.</span><span class="sxs-lookup"><span data-stu-id="6a466-114">This requires at least two Management Servers that appear to be a single Management Server.</span></span> <span data-ttu-id="6a466-115">Quando l'ambiente usa un cluster NLB con diversi server di gestione, è necessaria una configurazione avanzata del certificato usato per il cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="6a466-115">When your environment uses an NLB cluster with several Management Servers, you need an advanced configuration of the certificate used for the NLB cluster.</span></span>

<span data-ttu-id="6a466-116">Il certificato App-V viene inviato a un'autorità di certificazione (CA) configurata in un computer che utilizza Windows Server2003.</span><span class="sxs-lookup"><span data-stu-id="6a466-116">The App-V certificate is submitted to a certification authority (CA) that is configured on a computer running Windows Server2003.</span></span> <span data-ttu-id="6a466-117">La rete SAN consente di connettersi a un nome host del cluster NLB di Management Server specifico usando un nome DNS (Domain Name System) che potrebbe essere diverso dai nomi dei computer effettivi, perché possono essere presenti fino a 32 server che includono il cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="6a466-117">The SAN lets you connect to a specific Management Server NLB cluster host name by using a Domain Name System (DNS) name that might differ from the actual computer names, because there can be up to 32 servers that comprise the NLB cluster.</span></span>

<span data-ttu-id="6a466-118">Questa configurazione è necessaria solo quando si usa un cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="6a466-118">This configuration is necessary only when using an NLB cluster.</span></span> <span data-ttu-id="6a466-119">Quando il client si connette al server, si connetterà usando il nome di dominio completo (FQDN) del cluster NLB e non l'FQDN di un singolo server.</span><span class="sxs-lookup"><span data-stu-id="6a466-119">When the client connects to the server, it will connect using the fully qualified domain name (FQDN) of the NLB cluster and not the FQDN of an individual server.</span></span> <span data-ttu-id="6a466-120">Se non si aggiunge la proprietà SAN con il nome di dominio completo dei nodi del server nel cluster, tutte le connessioni client verranno rifiutate, perché il nome comune del certificato non corrisponde a quello del server.</span><span class="sxs-lookup"><span data-stu-id="6a466-120">If you do not add the SAN property with the FQDN of the server nodes in the cluster, all client connections are refused because the common name of the certificate won’t match the server name.</span></span>

<span data-ttu-id="6a466-121">Per informazioni più dettagliate sulla configurazione dei certificati con l'attributo SAN, vedere <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="6a466-121">For more detailed information about configuring certificates with the SAN attribute, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

## <span data-ttu-id="6a466-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a466-122">Related topics</span></span>


[<span data-ttu-id="6a466-123">Configurazione dei certificati per il supporto dello streaming sicuro</span><span class="sxs-lookup"><span data-stu-id="6a466-123">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

[<span data-ttu-id="6a466-124">Come modificare le autorizzazioni della chiave privata supportare Management Server o Streaming Server</span><span class="sxs-lookup"><span data-stu-id="6a466-124">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





