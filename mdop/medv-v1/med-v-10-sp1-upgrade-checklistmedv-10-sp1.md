---
title: Elenco di controllo per l'aggiornamento di MED-V 1.0 SP1
description: Elenco di controllo per l'aggiornamento di MED-V 1.0 SP1
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827266"
---
# <span data-ttu-id="c6c19-103">Elenco di controllo per l'aggiornamento di MED-V 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="c6c19-103">MED-V 1.0 SP1 Upgrade Checklist</span></span>


<span data-ttu-id="c6c19-104">Per aggiornare Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 to MED-V 1.0 Service Pack1 (SP1), è necessario aggiornare il client.</span><span class="sxs-lookup"><span data-stu-id="c6c19-104">To upgrade Microsoft Enterprise Desktop Virtualization (MED-V)1.0 to MED-V1.0 Service Pack1 (SP1), the client must be upgraded.</span></span> <span data-ttu-id="c6c19-105">Il server può essere aggiornato facoltativamente.</span><span class="sxs-lookup"><span data-stu-id="c6c19-105">The server can optionally be upgraded.</span></span>

## <span data-ttu-id="c6c19-106">Aggiornamento del server</span><span class="sxs-lookup"><span data-stu-id="c6c19-106">Server Upgrade</span></span>


**<span data-ttu-id="c6c19-107">Per aggiornare il server MED-V 1.0 a MED-V 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="c6c19-107">To upgrade the MED-V1.0 server to MED-V1.0 SP1</span></span>**

1.  <span data-ttu-id="c6c19-108">Eseguire il backup dei file seguenti che si trovano nella directory \* &lt; INSTALLDIR &gt; /Servers/ConfigurationServer\* :</span><span class="sxs-lookup"><span data-stu-id="c6c19-108">Back up the following files that are located in the *&lt;InstallDir&gt; / Servers / ConfigurationServer* directory:</span></span>

    -   <span data-ttu-id="c6c19-109">OrganizationalPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="c6c19-109">OrganizationalPolicy.XML</span></span>

    -   <span data-ttu-id="c6c19-110">ClientPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="c6c19-110">ClientPolicy.XML</span></span>

    -   <span data-ttu-id="c6c19-111">WorkspaceKeys.XML</span><span class="sxs-lookup"><span data-stu-id="c6c19-111">WorkspaceKeys.XML</span></span>

2.  <span data-ttu-id="c6c19-112">Eseguire il backup del file \* &lt; INSTALLDIR &gt; /Server/ServerSettings.xml\* .</span><span class="sxs-lookup"><span data-stu-id="c6c19-112">Back up the *&lt;InstallDir&gt; / Servers / ServerSettings.xml* file.</span></span>

3.  <span data-ttu-id="c6c19-113">Disinstallare il server MED-V 1.0.</span><span class="sxs-lookup"><span data-stu-id="c6c19-113">Uninstall the MED-V1.0 server.</span></span>

4.  <span data-ttu-id="c6c19-114">Installare il server MED-V 1.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c6c19-114">Install the MED-V1.0 SP1 server.</span></span>

5.  <span data-ttu-id="c6c19-115">Ripristinare i file di backup nelle directory appropriate.</span><span class="sxs-lookup"><span data-stu-id="c6c19-115">Restore the backup files to the appropriate directories.</span></span>

6.  <span data-ttu-id="c6c19-116">Riavviare il servizio server MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6c19-116">Restart the MED-V server service.</span></span>

<span data-ttu-id="c6c19-117">**Nota**  Se la configurazione del server è stata modificata rispetto all'impostazione predefinita, i file potrebbero essere archiviati in una posizione diversa.</span><span class="sxs-lookup"><span data-stu-id="c6c19-117">**Note** If the server configuration has been changed from the default, the files might be stored in a different location.</span></span>

 

## <span data-ttu-id="c6c19-118">Aggiornamento client</span><span class="sxs-lookup"><span data-stu-id="c6c19-118">Client Upgrade</span></span>


<span data-ttu-id="c6c19-119">Per aggiornare il client MED-V 1.0 a MED-V 1.0 SP1, installare il file msp in un client MED-V 1.0.</span><span class="sxs-lookup"><span data-stu-id="c6c19-119">To upgrade the MED-V1.0 client to MED-V1.0 SP1, install the .msp file on a MED-V1.0 client.</span></span> <span data-ttu-id="c6c19-120">Il client e il MED-V vengono aggiornati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c6c19-120">The client and MED-V are automatically upgraded.</span></span>

 

 





