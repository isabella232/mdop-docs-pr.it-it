---
title: Come configurare Bilanciamento carico di rete per MBAM
description: Come configurare Bilanciamento carico di rete per MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825515"
---
# <span data-ttu-id="d7e8e-103">Come configurare Bilanciamento carico di rete per MBAM</span><span class="sxs-lookup"><span data-stu-id="d7e8e-103">How to Configure Network Load Balancing for MBAM</span></span>


<span data-ttu-id="d7e8e-104">Per verificare che siano stati soddisfatti i prerequisiti e i requisiti hardware e software per installare la caratteristica server di amministrazione e monitoraggio, vedere [prerequisiti per la distribuzione di mbam 1,0](mbam-10-deployment-prerequisites.md) e le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="d7e8e-104">To verify that you have met the prerequisites and hardware and software requirements to install the Administration and Monitoring Server feature, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="d7e8e-105">**Nota**  Per ottenere i file di log della configurazione, è necessario installare Microsoft BitLocker Administration and Monitoring (MBAM) tramite il pacchetto **msiexec** e l'opzione di posizione **/l** &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="d7e8e-105">**Note** To obtain the setup log files, you must install Microsoft BitLocker Administration and Monitoring (MBAM) by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="d7e8e-106">I file di log vengono creati nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-106">The Log files are created in the location that you specify.</span></span>

<span data-ttu-id="d7e8e-107">I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% dell'utente che installa MBAM.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-107">Additional setup log files are created in the %temp% folder of the user who installs MBAM.</span></span>

 

<span data-ttu-id="d7e8e-108">I cluster di bilanciamento del carico di rete (NLB) per l'amministrazione e il server di monitoraggio offrono la scalabilità in MBAM e dovrebbe supportare più di 55.000 computer client MBAM.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-108">The Network Load Balancing (NLB) clusters for the Administration and Monitoring Server feature provides scalability in MBAM and it should support more than 55,000 MBAM client computers.</span></span>

<span data-ttu-id="d7e8e-109">**Nota**  Il bilanciamento del carico di rete di Windows Server distribuisce le richieste client in un set di server configurati in un singolo cluster di server.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-109">**Note** Windows Server Network Load Balancing distributes client requests across a set of servers that are configured into a single server cluster.</span></span> <span data-ttu-id="d7e8e-110">Quando il bilanciamento del carico di rete viene installato in ognuno dei server (host) in un cluster, il cluster presenta un indirizzo IP virtuale o un nome di dominio completo (FQDN) alle richieste del cliente.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-110">When Network Load Balancing is installed on each of the servers (hosts) in a cluster, the cluster presents a virtual IP address or fully qualified domain name (FQDN) to client requests.</span></span> <span data-ttu-id="d7e8e-111">Le richieste client iniziali vengono inviate a tutti gli host del cluster, ma solo un host accetta e gestisce la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-111">The initial client requests go to all the hosts in the cluster, but only one host accepts and handles the request.</span></span>

<span data-ttu-id="d7e8e-112">Tutti i computer che faranno parte di un cluster NLB avranno i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7e8e-112">All computers that will be part of a NLB cluster have the following requirements:</span></span>

-   <span data-ttu-id="d7e8e-113">Tutti i computer nel cluster NLB devono essere nello stesso dominio.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-113">All computers in the NLB cluster must be in the same domain.</span></span>

-   <span data-ttu-id="d7e8e-114">Ogni computer nel cluster NLB deve usare un indirizzo IP statico.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-114">Each computer in the NLB cluster must use a static IP address.</span></span>

-   <span data-ttu-id="d7e8e-115">Ogni computer nel cluster NLB deve avere il bilanciamento del carico di rete abilitato.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-115">Each computer in the NLB cluster must have Network Load Balancing enabled.</span></span>

-   <span data-ttu-id="d7e8e-116">Il cluster NLB richiede un indirizzo IP statico e un record host deve essere creato manualmente nel DNS (Domain Name System).</span><span class="sxs-lookup"><span data-stu-id="d7e8e-116">The NLB cluster requires a static IP address, and a host record must be manually created in the domain name system (DNS).</span></span>

 

## <span data-ttu-id="d7e8e-117">Configurazione del bilanciamento del carico di rete per i server di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="d7e8e-117">Configuring Network Load Balancing for MBAM Administration and Monitoring Servers</span></span>


<span data-ttu-id="d7e8e-118">I passaggi seguenti descrivono come configurare un nome virtuale del cluster NLB e un indirizzo IP per due server di amministrazione e monitoraggio di MBAM e come configurare i client MBAM per l'uso del cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-118">The following steps describe how to configure an NLB cluster virtual name and IP address for two MBAM Administration and Monitoring servers, and how to configure MBAM Clients to use the NLB Cluster.</span></span>

<span data-ttu-id="d7e8e-119">Prima di iniziare le procedure descritte in questo argomento, è necessario che la funzionalità MBAM Administration e Monitoring Server sia stata installata correttamente usando lo stesso binding della porta di IIS in due computer server distinti che soddisfano i prerequisiti per l'installazione delle funzionalità di MBAM server e la configurazione del cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-119">Before you begin the procedures described in this topic, you must have the MBAM Administration and Monitoring Server feature successfully installed by using the same IIS port binding on two separate server computers that meet the prerequisites for both MBAM Server feature installation and NLB Cluster configuration.</span></span>

<span data-ttu-id="d7e8e-120">**Nota**  Questo argomento descrive il processo di base dell'uso di Gestione bilanciamento carico di rete per creare un cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-120">**Note** This topic describes the basic process of using Network Load Balancing Manager to create an NLB Cluster.</span></span> <span data-ttu-id="d7e8e-121">La procedura esatta per configurare un server Windows come parte di un cluster NLB dipende dalla versione di Windows Server in uso.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-121">The exact steps to configure a Windows Server as part of an NLB cluster depend on the Windows Server version in use..</span></span> <span data-ttu-id="d7e8e-122">Per altre informazioni su come creare NLBs in WindowsServer2008, vedere [creazione di cluster di bilanciamento del carico di rete](https://go.microsoft.com/fwlink/?LinkId=197176) nella raccolta TechNet di Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-122">For more information about how to create NLBs on WindowsServer2008, see [Creating Network Load Balancing Clusters](https://go.microsoft.com/fwlink/?LinkId=197176) in the Windows Server2008 TechNet library.</span></span>

 

**<span data-ttu-id="d7e8e-123">Per configurare un nome virtuale del cluster NLB e un indirizzo IP per due server di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="d7e8e-123">To configure an NLB Cluster Virtual Name and IP address for two MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="d7e8e-124">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **strumenti di amministrazione**e quindi fare clic su **Gestione bilanciamento carico di rete**.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-124">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Network Load Balancing Manager**.</span></span>

    <span data-ttu-id="d7e8e-125">**Nota**  Se il gestore NLB non è presente, è possibile installarlo come caratteristica WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-125">**Note** If the NLB Manager is not present, you can install it as a WindowsServer feature.</span></span> <span data-ttu-id="d7e8e-126">È necessario installare questa funzionalità sia in amministrazione MBAM che in server di monitoraggio se si vuole configurarla nel cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-126">You must install this feature on both MBAM Administration and Monitoring servers if you want to configure it into the NLB cluster.</span></span>

     

2.  <span data-ttu-id="d7e8e-127">Sulla barra dei menu fare clic su **cluster**e quindi su **nuovo** per aprire la finestra di dialogo **parametri cluster** .</span><span class="sxs-lookup"><span data-stu-id="d7e8e-127">On the menu bar, click **Cluster**, and then click **New** to open the **Cluster Parameters** dialog box.</span></span>

3.  <span data-ttu-id="d7e8e-128">Nella finestra di dialogo **parametri cluster** immettere le informazioni per la configurazione IP del cluster NLB:</span><span class="sxs-lookup"><span data-stu-id="d7e8e-128">In the **Cluster Parameters** dialog box, enter the information for the NLB cluster IP configuration:</span></span>

    -   <span data-ttu-id="d7e8e-129">**Indirizzo IP:** Indirizzo IP del cluster NLB registrato nel DNS</span><span class="sxs-lookup"><span data-stu-id="d7e8e-129">**IP address:** NLB cluster IP address registered in DNS</span></span>

    -   <span data-ttu-id="d7e8e-130">**Subnet mask:** Subnet mask dell'indirizzo IP del cluster NLB registrato nel DNS</span><span class="sxs-lookup"><span data-stu-id="d7e8e-130">**Subnet mask:** NLB cluster IP address subnet mask registered in DNS</span></span>

    -   <span data-ttu-id="d7e8e-131">**Nome Internet completo:** FQDN del nome del cluster NLB registrato in DNS</span><span class="sxs-lookup"><span data-stu-id="d7e8e-131">**Full Internet name:** FQDN of NLB cluster name registered in DNS</span></span>

4.  <span data-ttu-id="d7e8e-132">Verificare che l'opzione **unicast** sia selezionata in **modalità operazione cluster**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-132">Ensure that **Unicast** is selected in **Cluster operation mode**, and then click **Next**.</span></span>

5.  <span data-ttu-id="d7e8e-133">Nella pagina **indirizzi IP del cluster** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-133">On the **Cluster IP Addresses** page, click **Next**.</span></span>

6.  <span data-ttu-id="d7e8e-134">Nella pagina **regole porta** fare clic su **modifica** per definire le porte a cui il cluster NLB risponderà e configurare le porte usate per la comunicazione del sistema da client a sito mentre sono definite per il sito oppure fare clic su **Avanti** per abilitare l'indirizzo IP del cluster NLB per rispondere a tutte le porte TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-134">On the **Port Rules** page, click **Edit** to define the ports that the NLB cluster will respond to and configure the ports that are used for client-to-site system communication as they are defined for the site, or click **Next** to enable the NLB cluster IP address to respond to all TCP/IP ports.</span></span>

    <span data-ttu-id="d7e8e-135">**Nota**  Verificare che l' **affinità** sia impostata su **Single**.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-135">**Note** Ensure that **Affinity** is set to **Single**.</span></span>

     

7.  <span data-ttu-id="d7e8e-136">Nella pagina **Connect** immettere un nome host dell'istanza di amministrazione e monitoraggio di mbam che farà parte del cluster NLB in **host**e quindi fare clic su **Connetti**.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-136">On the **Connect** page, enter an MBAM Administration and Monitoring server instance host name that will be part of the NLB cluster in **Host**, and then click **Connect**.</span></span>

8.  <span data-ttu-id="d7e8e-137">Nelle **interfacce disponibili per la configurazione di un nuovo cluster**selezionare l'interfaccia di rete che verrà configurata per rispondere alla comunicazione cluster NLB e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-137">In **Interfaces available for configuring a new cluster**, select the networking interface that will be configured to respond to NLB cluster communication, and then click **Next**.</span></span>

9.  <span data-ttu-id="d7e8e-138">Nella pagina **Host Parameters** esaminare le informazioni visualizzate per verificare che le impostazioni di **configurazione IP dedicate** VISUALIZZino la configurazione IP dell'host dedicato per l'host del cluster NLB corretto, verificare che lo stato dell'host iniziale sia quello **predefinito:** viene **avviato**e quindi fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-138">On the **Host Parameters** page, review the information displayed to ensure that the **Dedicated IP configuration** settings display the dedicated host IP configuration for the correct NLB cluster host, check that the Initial host state **Default state:** is **Started**, and then click **Finish**.</span></span>

    <span data-ttu-id="d7e8e-139">**Nota**  Nella pagina **parametri host** viene visualizzata anche la priorità dell'host del cluster NLB, che è da 1 a 32.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-139">**Note** The **Host Parameters** page also displays the NLB cluster host priority, which is 1 through 32.</span></span> <span data-ttu-id="d7e8e-140">Man mano che i nuovi host vengono aggiunti al cluster NLB, la priorità dell'host deve essere diversa dagli host aggiunti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-140">As new hosts are added to the NLB cluster, the host priority must differ from the previously added hosts.</span></span> <span data-ttu-id="d7e8e-141">La priorità viene incrementata automaticamente quando si usa Gestione bilanciamento carico di rete.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-141">The priority is automatically incremented when you use the Network Load Balancing Manager.</span></span>

     

10. <span data-ttu-id="d7e8e-142">Fare clic su \*\* &lt; nome &gt; cluster NLB\*\* e verificare che lo **stato** dell'interfaccia host NLB venga visualizzato **convergente** prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-142">Click **&lt;NLB cluster name&gt;** and ensure that the NLB host interface **Status** displays **Converged** before you continue.</span></span> <span data-ttu-id="d7e8e-143">Questo passaggio può richiedere che il cluster NLB venga aggiornato come configurazione TCP/IP dell'host che viene modificata da gestione NLB.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-143">This step might require that you refresh the NLB cluster display as the host TCP/IP configuration that is being modified by the NLB Manager.</span></span>

11. <span data-ttu-id="d7e8e-144">Per aggiungere altri host al cluster NLB, fare clic con il pulsante destro del mouse su \*\* &lt; nome &gt; cluster NLB\*\*, scegliere **Aggiungi host a cluster** e quindi ripetere i passaggi da 7 a 10 per ogni sistema di sito che farà parte del cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-144">To add additional hosts to the NLB cluster, right-click **&lt;NLB cluster name&gt;**, click **Add Host to Cluster,** and then repeat steps 7 through 10 for each site system that will be part of the NLB cluster.</span></span>

12. <span data-ttu-id="d7e8e-145">In un computer in cui è installato MBAM modello di criteri di gruppo, modificare le impostazioni dei criteri di gruppo di mbam per configurare gli endpoint di servizi di MBAM per usare il nome del cluster NLB e il binding della porta IIS appropriato per accedere alle funzionalità di amministrazione e monitoraggio di MBAM che vengono installate nei computer del cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-145">On a computer that has MBAM Group Policy template installed, modify the MBAM Group Policy settings to configure the MBAM services endpoints to use the NLB Cluster name and the appropriate IIS port binding to access the MBAM Administration and Monitoring Server features that are installed on the NLB Cluster computers.</span></span> <span data-ttu-id="d7e8e-146">Per altre informazioni su come modificare le impostazioni dei GPO di MBAM, Vedi [come modificare le impostazioni di gpo 1,0](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d7e8e-146">For more information about how to edit MBAM GPO settings, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span> <span data-ttu-id="d7e8e-147">Se i server di amministrazione e monitoraggio di MBAM sono nuovi per l'ambiente, verificare che le appartenenze del gruppo di sicurezza locale richiesto siano state configurate correttamente.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-147">If the MBAM Administration and Monitoring servers are new to your environment, ensure that the required local security group memberships have been properly configured.</span></span> <span data-ttu-id="d7e8e-148">Per altre informazioni sui requisiti per il gruppo di sicurezza, vedere [pianificazione dei ruoli di amministratore di MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="d7e8e-148">For more information about security group requirements, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

13. <span data-ttu-id="d7e8e-149">Una volta completata la configurazione del cluster NLB, è consigliabile verificare che il cluster NLB di amministrazione e monitoraggio sia funzionale.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-149">When the NLB Cluster configuration is complete, we recommend that you validate that the MBAM Administration and Monitoring NLB Cluster is functional.</span></span> <span data-ttu-id="d7e8e-150">A questo scopo, aprire un Web browser in un computer diverso dai server configurati in NLB e verificare che sia possibile accedere al sito Web di amministrazione e monitoraggio di MBAM tramite il nome di dominio completo NLB.</span><span class="sxs-lookup"><span data-stu-id="d7e8e-150">To do this, open a web browser on a computer other than the servers that are configured in the NLB, and ensure that you can access the MBAM Administration and Monitoring web site by using the NLB FQDN.</span></span>

## <span data-ttu-id="d7e8e-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7e8e-151">Related topics</span></span>


[<span data-ttu-id="d7e8e-152">Distribuzione dell'infrastruttura server di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="d7e8e-152">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





