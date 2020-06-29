---
title: Configurazione del server MED-V per la modalità cluster
description: Configurazione del server MED-V per la modalità cluster
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826716"
---
# <span data-ttu-id="491e4-103">Configurazione del server MED-V per la modalità cluster</span><span class="sxs-lookup"><span data-stu-id="491e4-103">Configuring MED-V Server for Cluster Mode</span></span>


<span data-ttu-id="491e4-104">È possibile configurare il server MED-V in modalità cluster.</span><span class="sxs-lookup"><span data-stu-id="491e4-104">You can configure the MED-V server in cluster mode.</span></span> <span data-ttu-id="491e4-105">In modalità cluster vengono usati due server e tutti i file identificati come reciproci per entrambi i server vengono posizionati in un file System.</span><span class="sxs-lookup"><span data-stu-id="491e4-105">In cluster mode, two servers are used and all files identified as mutual to both servers are placed on a file system.</span></span> <span data-ttu-id="491e4-106">Il server accede ai file dal file System anziché archiviare localmente i file.</span><span class="sxs-lookup"><span data-stu-id="491e4-106">The server accesses the files from the file system rather than storing the files locally.</span></span>

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**<span data-ttu-id="491e4-107">Per configurare il server MED-V in modalità cluster</span><span class="sxs-lookup"><span data-stu-id="491e4-107">To configure the MED-V server in cluster mode</span></span>**

1.  <span data-ttu-id="491e4-108">Installare e configurare MED-V in uno dei server.</span><span class="sxs-lookup"><span data-stu-id="491e4-108">Install and configure MED-V on one of the servers.</span></span>

2.  <span data-ttu-id="491e4-109">Creare una rete condivisa in una posizione centrale in cui tutti i server possono accedervi.</span><span class="sxs-lookup"><span data-stu-id="491e4-109">Create a shared network in a central location where all of the servers can access it.</span></span>

3.  <span data-ttu-id="491e4-110">Copiare il contenuto della cartella \* &lt; INSTALLDIR &gt; /Servers/ConfigurationServer\* nella rete condivisa.</span><span class="sxs-lookup"><span data-stu-id="491e4-110">Copy the contents of the *&lt;InstallDir&gt;/Servers/ConfigurationServer* folder to the shared network.</span></span>

4.  <span data-ttu-id="491e4-111">Installare il server MED-V in tutti i server designati.</span><span class="sxs-lookup"><span data-stu-id="491e4-111">Install MED-V server on all designated servers.</span></span>

5.  <span data-ttu-id="491e4-112">Nella rete condivisa assegnare l'accesso completo a tutti gli account di sistema di MED-V Server.</span><span class="sxs-lookup"><span data-stu-id="491e4-112">On the shared network, assign full access to all MED-V server system accounts.</span></span>

6.  <span data-ttu-id="491e4-113">In ogni server eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="491e4-113">On each server, do the following:</span></span>

    1.  <span data-ttu-id="491e4-114">Nel file \* &lt; InstallDir &gt; /Servers/ServerConfiguration.xml\* impostare il valore di \* &lt; PercorsoArchivio &gt; \* sul percorso di rete condiviso.</span><span class="sxs-lookup"><span data-stu-id="491e4-114">In the *&lt;InstallDir&gt;/Servers/ServerConfiguration.xml* file, set the value of *&lt;StorePath&gt;* to the shared network path.</span></span>

    2.  <span data-ttu-id="491e4-115">Copiare il file di \* &lt; &gt; KeyPair.xml/Servers/InstsallDir\* dal server originale a tutti i server MED-V.</span><span class="sxs-lookup"><span data-stu-id="491e4-115">Copy the *&lt;InstsallDir&gt;/Servers/KeyPair.xml* file from the original server to all MED-V servers.</span></span>

    3.  <span data-ttu-id="491e4-116">Riavviare il servizio MED-V.</span><span class="sxs-lookup"><span data-stu-id="491e4-116">Restart the MED-V service.</span></span>

<span data-ttu-id="491e4-117">**Nota**  Se tutti i server hanno le stesse impostazioni locali, ad esempio le porte in attesa, il server IIS, le autorizzazioni di gestione, il database del report e così via, la \* &lt; &gt; ServerSettings.xmlInstallDir/Servers/\* può essere condivisa anche da tutti i server.</span><span class="sxs-lookup"><span data-stu-id="491e4-117">**Note** If all servers have the same local settings (such as listening ports, IIS server, management permissions, report database, and so on), the *&lt;InstallDir&gt;/Servers/ServerSettings.xml* can be shared by all servers as well.</span></span>

 

## <span data-ttu-id="491e4-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="491e4-118">Related topics</span></span>


[<span data-ttu-id="491e4-119">Progettazione e pianificazione dell'infrastruttura MED-V</span><span class="sxs-lookup"><span data-stu-id="491e4-119">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





