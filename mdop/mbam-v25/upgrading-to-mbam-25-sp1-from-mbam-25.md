---
title: Aggiornamento a MBAM 2.5 SP1 da MBAM 2.5
description: Aggiornamento a MBAM 2.5 SP1 da MBAM 2.5
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 19da3df0976b51700e0d10c302a31421a88d17e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804456"
---
# <span data-ttu-id="d0169-103">Aggiornamento a MBAM 2.5 SP1 da MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d0169-103">Upgrading to MBAM 2.5 SP1 from MBAM 2.5</span></span>
<span data-ttu-id="d0169-104">Questo argomento descrive il processo per l'aggiornamento di Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 e il client MBAM da 2,5 a MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="d0169-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 and the MBAM Client from 2.5 to MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="d0169-105">Prima di iniziare</span><span class="sxs-lookup"><span data-stu-id="d0169-105">Before you begin</span></span>
#### <span data-ttu-id="d0169-106">Scaricare la versione di manutenzione di maggio 2019</span><span class="sxs-lookup"><span data-stu-id="d0169-106">Download the May 2019 servicing release</span></span>
[<span data-ttu-id="d0169-107">Pacchetto di ottimizzazione desktop</span><span class="sxs-lookup"><span data-stu-id="d0169-107">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=58345)

#### <span data-ttu-id="d0169-108">Verificare la documentazione dell'installazione</span><span class="sxs-lookup"><span data-stu-id="d0169-108">Verify the installation documentaion</span></span>
<span data-ttu-id="d0169-109">Verificare di avere una documentazione corrente dell'ambiente MBAM, inclusi tutti i nomi dei server, i nomi di database, gli account del servizio e le relative password.</span><span class="sxs-lookup"><span data-stu-id="d0169-109">Verify you have a current documentation of your MBAM environment, including all server names, database names, service accounts and their passwords.</span></span>

### <span data-ttu-id="d0169-110">Passaggi di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d0169-110">Upgrade steps</span></span>
#### <span data-ttu-id="d0169-111">Procedura per aggiornare il database MBAM (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="d0169-111">Steps to upgrade the MBAM Database (SQL Server)</span></span>
1. <span data-ttu-id="d0169-112">Uso di MBAM Configurator; rimuovere il ruolo report da SQL Server o ovunque sia ospitato il database SSRS.</span><span class="sxs-lookup"><span data-stu-id="d0169-112">Using the MBAM Configurator; remove the Reports role from the SQL server, or wherever the SSRS database is hosted.</span></span> <span data-ttu-id="d0169-113">A seconda dell'ambiente, può essere lo stesso server o uno separato.</span><span class="sxs-lookup"><span data-stu-id="d0169-113">Depending on your environment, this can be the same server or a separate one.</span></span>
  > [!NOTE]
  > <span data-ttu-id="d0169-114">Non verrà visualizzata un'opzione per rimuovere i database; Questo è previsto.</span><span class="sxs-lookup"><span data-stu-id="d0169-114">You will not see an option to remove the Databases; this is expected.</span></span>  
2. <span data-ttu-id="d0169-115">Installare 2,5 SP1 (che si trova in MDOP-Microsoft Desktop Optimization Pack 2015 dal sito Centro servizi Volume Licensing:</span><span class="sxs-lookup"><span data-stu-id="d0169-115">Install 2.5 SP1(Located with MDOP - Microsoft Desktop Optimization Pack 2015 from the Volume Licensing Service Center site:</span></span>  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. <span data-ttu-id="d0169-116">Non configurarlo in questo momento</span><span class="sxs-lookup"><span data-stu-id="d0169-116">Do not configure it at this time</span></span> 
4. <span data-ttu-id="d0169-117">Uso di MBAM Configurator; aggiungere di nuovo il ruolo report</span><span class="sxs-lookup"><span data-stu-id="d0169-117">Using the MBAM Configurator; re-add the Reports role</span></span>
5. <span data-ttu-id="d0169-118">Uso di MBAM Configurator; aggiungere di nuovo il ruolo di database SQL in SQL Server</span><span class="sxs-lookup"><span data-stu-id="d0169-118">Using the MBAM Configurator; re-add the SQL Database role on the SQL Server</span></span>
6. <span data-ttu-id="d0169-119">Alla fine, sarai avvisato che la DBs esiste già e non è stata creata, ma questo è previsto</span><span class="sxs-lookup"><span data-stu-id="d0169-119">At the end, you will be warned that the DBs already exist and  weren’t created, but this is expected</span></span>
7. <span data-ttu-id="d0169-120">Questo processo aggiorna i database esistenti alla versione corrente in fase di installazione.</span><span class="sxs-lookup"><span data-stu-id="d0169-120">This process updates the existing databases to the current version being installed.</span></span>              

#### <span data-ttu-id="d0169-121">Procedura per aggiornare il server MBAM (in uso MBAM e IIS)</span><span class="sxs-lookup"><span data-stu-id="d0169-121">Steps to upgrade the MBAM Server (Running MBAM and IIS)</span></span>
1. <span data-ttu-id="d0169-122">Uso di MBAM Configurator; rimuovere i portali amministratore e self service dal server IIS</span><span class="sxs-lookup"><span data-stu-id="d0169-122">Using the MBAM Configurator; remove the Admin and Self Service Portals from  the IIS server</span></span>
2. <span data-ttu-id="d0169-123">Installare MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="d0169-123">Install MBAM 2.5 SP1</span></span>
3. <span data-ttu-id="d0169-124">Non configurarlo in questo momento</span><span class="sxs-lookup"><span data-stu-id="d0169-124">Do not configure it at this time</span></span>  
4. <span data-ttu-id="d0169-125">Uso di MBAM Configurator; aggiungere di nuovo i portali amministratore e self service al server IIS</span><span class="sxs-lookup"><span data-stu-id="d0169-125">Using the MBAM Configurator; re-add the Admin and Self Service Portals to the IIS server</span></span> 
5. <span data-ttu-id="d0169-126">Aprire un prompt dei comandi con privilegi elevati, digitare **iisreset**e premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="d0169-126">Open an elevated command prompt, type **IISRESET**, and hit Enter.</span></span>
 
#### <span data-ttu-id="d0169-127">Procedura per aggiornare i client e gli endpoint di MBAM</span><span class="sxs-lookup"><span data-stu-id="d0169-127">Steps to upgrade the MBAM Clients/Endpoints</span></span>
1. <span data-ttu-id="d0169-128">Disinstallare l'agente 2,5 dagli endpoint client</span><span class="sxs-lookup"><span data-stu-id="d0169-128">Uninstall the 2.5 Agent from client endpoints</span></span>
2. <span data-ttu-id="d0169-129">Installare l'agente di 2,5 SP1 negli endpoint client</span><span class="sxs-lookup"><span data-stu-id="d0169-129">Install the 2.5 SP1 Agent on the client endpoints</span></span>
3. <span data-ttu-id="d0169-130">Spingere l'aggiornamento del client rollup di maggio 2019 ai client che utilizzano l'agente 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="d0169-130">Push out the May 2019 Rollup Client update to clients running the 2.5 SP1 Agent</span></span> 
4. <span data-ttu-id="d0169-131">Non è necessario disinstallare il client esistente prima di installare il rollup di 2019 di maggio.</span><span class="sxs-lookup"><span data-stu-id="d0169-131">There is no need to uninstall the existing client prior to installing the May 2019 Rollup.</span></span>  
