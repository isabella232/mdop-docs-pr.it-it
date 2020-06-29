---
title: Procedure consigliate per le operazioni MED-V
description: Procedure consigliate per le operazioni MED-V
author: dansimp
ms.assetid: 231e2b9a-8b49-42fe-93b5-2ef12fe17bac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4353a15c756dba8cf44f530c2077546e3f9288cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825396"
---
# <span data-ttu-id="59886-103">Procedure consigliate per le operazioni MED-V</span><span class="sxs-lookup"><span data-stu-id="59886-103">Security Best Practices for MED-V Operations</span></span>


<span data-ttu-id="59886-104">In qualità di amministratore autorizzato, è responsabile proteggere le informazioni degli utenti e mantenere la sicurezza dell'organizzazione durante e dopo la distribuzione delle aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="59886-104">As an authorized administrator, you are responsible to protect the information of the users and maintain security of your organization during and after the deployment of MED-V workspaces.</span></span> <span data-ttu-id="59886-105">In particolare, prendere in considerazione i problemi seguenti.</span><span class="sxs-lookup"><span data-stu-id="59886-105">In particular, consider the following issues.</span></span>

<span data-ttu-id="59886-106">**Personalizzazione di Internet Explorer nell'area di lavoro MED-V**.</span><span class="sxs-lookup"><span data-stu-id="59886-106">**Customizing Internet Explorer in the MED-V workspace**.</span></span> <span data-ttu-id="59886-107">Le versioni precedenti del sistema operativo Windows e di Internet Explorer non sono sicure come le versioni correnti.</span><span class="sxs-lookup"><span data-stu-id="59886-107">Earlier versions of the Windows operating system and of Internet Explorer are not as secure as current versions.</span></span> <span data-ttu-id="59886-108">Di conseguenza, Internet Explorer nell'area di lavoro MED-V è configurato per impedire l'esplorazione e altre attività che possono rappresentare rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="59886-108">Therefore, Internet Explorer in the MED-V workspace is configured to prevent browsing and other activities that can pose security risks.</span></span> <span data-ttu-id="59886-109">Inoltre, l'impostazione dell'area di sicurezza Internet per Internet Explorer nell'area di lavoro MED-V è impostata sul livello più alto.</span><span class="sxs-lookup"><span data-stu-id="59886-109">In addition, the Internet security zone setting for Internet Explorer in the MED-V workspace is set to the highest level.</span></span> <span data-ttu-id="59886-110">Per impostazione predefinita, entrambe le configurazioni vengono impostate nel Packager area di lavoro MED-V quando si crea il pacchetto dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="59886-110">By default, both of these configurations are set in the MED-V Workspace Packager when you create your MED-V workspace package.</span></span>

<span data-ttu-id="59886-111">Utilizzando Internet Explorer Administration Kit (IEAK) o modificando le impostazioni predefinite nel Packager area di lavoro MED-V, è possibile personalizzare Internet Explorer nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="59886-111">By using Internet Explorer Administration Kit (IEAK) or by changing the defaults in the MED-V Workspace Packager, you can customize Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="59886-112">Tuttavia, rendersi conto che se si personalizza Internet Explorer nell'area di lavoro MED-V in modo da renderla meno sicura, è possibile esporre l'organizzazione a tali rischi per la sicurezza presenti nelle versioni precedenti di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="59886-112">However, realize that if you customize Internet Explorer in the MED-V workspace in such a way as to make it less secure, you can expose your organization to those security risks that are present in older versions of Internet Explorer.</span></span>

<span data-ttu-id="59886-113">Da un punto di vista della sicurezza, le procedure consigliate per la gestione di Internet Explorer nell'area di lavoro MED-V sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="59886-113">From a security perspective, best practices for managing Internet Explorer in the MED-V workspace are as follows:</span></span>

-   <span data-ttu-id="59886-114">Quando si crea il pacchetto dell'area di lavoro MED-V, uscire dal set di impostazioni predefinite in modo che Internet Explorer nell'area di lavoro MED-V sia configurato per impedire l'esplorazione e altre attività che possono rappresentare rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="59886-114">When creating your MED-V workspace package, leave the defaults set so that Internet Explorer in the MED-V workspace is configured to prevent browsing and other activities that can pose security risks.</span></span>

-   <span data-ttu-id="59886-115">Quando si crea il pacchetto dell'area di lavoro MED-V, uscire dal set di impostazioni predefinite in modo che l'impostazione di sicurezza per l'area di sicurezza Internet rimanga al massimo livello.</span><span class="sxs-lookup"><span data-stu-id="59886-115">When creating your MED-V workspace package, leave the defaults set so that the security setting for the Internet security zone remains at the highest level.</span></span>

-   <span data-ttu-id="59886-116">Configurare il proxy aziendale o il Content Advisor di Internet Explorer per bloccare i domini esterni alla rete Intranet aziendale.</span><span class="sxs-lookup"><span data-stu-id="59886-116">Configure your enterprise proxy or Internet Explorer Content Advisor to block domains that are outside your company’s intranet.</span></span>

**<span data-ttu-id="59886-117">Configurazione di un'area di lavoro MED-V per tutti gli utenti in un computer condiviso.</span><span class="sxs-lookup"><span data-stu-id="59886-117">Configuring a MED-V workspace for all users on a shared computer.</span></span>** <span data-ttu-id="59886-118">Quando si configura un'area di lavoro MED-V in modo che sia possibile accedervi da tutti gli utenti in un computer condiviso, si renderà conto che la macchina virtuale guest viene inserita in una posizione che offre l'accesso in lettura e scrittura a tutti gli utenti del sistema.</span><span class="sxs-lookup"><span data-stu-id="59886-118">When configuring a MED-V workspace so that it can be accessed by all users on a shared computer, realize that the guest virtual machine (VHD) is put in a location that gives Read and Write access to all users on that system.</span></span>

**<span data-ttu-id="59886-119">Configurazione di un account proxy per l'aggiunta di domini.</span><span class="sxs-lookup"><span data-stu-id="59886-119">Configuring a proxy account for domain joining.</span></span>** <span data-ttu-id="59886-120">Quando si configura un account proxy per l'aggiunta di macchine virtuali al dominio, è necessario sapere che l'utente finale può ottenere le credenziali dell'account proxy.</span><span class="sxs-lookup"><span data-stu-id="59886-120">When configuring a proxy account for joining virtual machines to the domain, you must know that it is possible for an end user to obtain the proxy account credentials.</span></span> <span data-ttu-id="59886-121">Occorre pertanto prendere precauzioni necessarie, ad esempio limitare i diritti degli utenti dell'account, per evitare che un utente finale usi le credenziali per causare danni.</span><span class="sxs-lookup"><span data-stu-id="59886-121">Thus, necessary precautions must be taken, such as limiting account user rights, to prevent an end user from using the credentials for causing harm.</span></span>

**<span data-ttu-id="59886-122">Configurazione Sysprep.</span><span class="sxs-lookup"><span data-stu-id="59886-122">Sysprep Configuration.</span></span>** <span data-ttu-id="59886-123">Anche se il file Sysprep. inf viene crittografato per impostazione predefinita, il contenuto può essere decrittografato e letto da qualsiasi utente finale determinato che possa accedere correttamente alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="59886-123">Although the Sysprep.inf file is encrypted by default, its contents can be decrypted and read by any determined end user who can successfully log on to the virtual machine.</span></span> <span data-ttu-id="59886-124">In questo articolo vengono generate preoccupazioni per la sicurezza perché il file Sysprep. inf può contenere credenziali oltre a un codice Product Key di Windows.</span><span class="sxs-lookup"><span data-stu-id="59886-124">This raises security concerns because the Sysprep.inf file can contain credentials in addition to a Windows product key.</span></span>

<span data-ttu-id="59886-125">È possibile ridurre questo rischio impostando un account limitato per l'aggiunta di macchine virtuali al dominio e specificando le credenziali per tale account durante la configurazione di Sysprep.</span><span class="sxs-lookup"><span data-stu-id="59886-125">You can lessen this risk by setting up a limited account for joining virtual machines to the domain and specifying the credentials for that account when configuring Sysprep.</span></span> <span data-ttu-id="59886-126">In alternativa, è anche possibile configurare Sysprep e la configurazione per la prima volta per l'esecuzione in modalità **assistita** e richiedere agli utenti finali di specificare le proprie credenziali per l'aggiunta della macchina virtuale al dominio.</span><span class="sxs-lookup"><span data-stu-id="59886-126">Alternately, you can also configure Sysprep and first time setup to run in **Attended** mode and require end users to provide their credentials for joining the virtual machine to the domain.</span></span>

<span data-ttu-id="59886-127">Una procedura consigliata per MED-V consiste nel specificare che FtsCompletion.exe venga eseguito con un account che conferisce ai diritti degli utenti finali la connessione al Guest tramite il client di connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="59886-127">A MED-V best practice is to specify that FtsCompletion.exe is run under an account that gives the end user rights to connect to the guest through the Remote Desktop Connection (RDC) Client.</span></span>

**<span data-ttu-id="59886-128">Autenticazione dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="59886-128">End-user authentication.</span></span>** <span data-ttu-id="59886-129">L'abilitazione della memorizzazione nella cache delle credenziali degli utenti finali offre la migliore esperienza utente di MED-V, ma crea il potenziale per cui qualcuno potrebbe avere accesso alle credenziali dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="59886-129">Enabling the caching of end-user credentials provides the best user experience of MED-V, but creates the potential that someone could gain access to the end user’s credentials.</span></span> <span data-ttu-id="59886-130">L'unico modo per ridurre il rischio è specificare nel **Packager area di lavoro MED-V** che le credenziali dell'utente finale non sono archiviate.</span><span class="sxs-lookup"><span data-stu-id="59886-130">The only way to lessen this risk is by specifying on the **MED-V Workspace Packager** that end-user credentials are not stored.</span></span> <span data-ttu-id="59886-131">Per altre informazioni sull'autenticazione degli utenti finali, vedere [autenticazione degli utenti finali di MED-V](authentication-of-med-v-end-users.md).</span><span class="sxs-lookup"><span data-stu-id="59886-131">For more information about authentication of end users, see [Authentication of MED-V End Users](authentication-of-med-v-end-users.md).</span></span>

## <span data-ttu-id="59886-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59886-132">Related topics</span></span>


[<span data-ttu-id="59886-133">Risoluzione dei problemi relativi alle operazioni</span><span class="sxs-lookup"><span data-stu-id="59886-133">Operations Troubleshooting</span></span>](operations-troubleshooting-medv2.md)

[<span data-ttu-id="59886-134">Microsoft Enterprise Desktop Virtualization 2,0</span><span class="sxs-lookup"><span data-stu-id="59886-134">Microsoft Enterprise Desktop Virtualization 2.0</span></span>](index.md)

 

 





