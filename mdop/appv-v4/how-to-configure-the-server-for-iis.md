---
title: Come configurare il server per IIS
description: Come configurare il server per IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817745"
---
# <span data-ttu-id="51b0e-103">Come configurare il server per IIS</span><span class="sxs-lookup"><span data-stu-id="51b0e-103">How to Configure the Server for IIS</span></span>


<span data-ttu-id="51b0e-104">Prima che le applicazioni virtuali possano essere trasmesse al client Desktop Application Virtualization e al client per Servizi Desktop remoto (in precedenza Servizi terminal), è necessario configurare i server IIS.</span><span class="sxs-lookup"><span data-stu-id="51b0e-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services), the IIS servers must be configured.</span></span> <span data-ttu-id="51b0e-105">Quando configuri i server, stai configurando la directory di contenuto in cui vengono caricati e archiviati i file SFT.</span><span class="sxs-lookup"><span data-stu-id="51b0e-105">When you configure the servers, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="51b0e-106">I file SFT contengono l'applicazione virtuale (o le applicazioni).</span><span class="sxs-lookup"><span data-stu-id="51b0e-106">The SFT files contain the virtual application (or applications).</span></span>

**<span data-ttu-id="51b0e-107">Per configurare la directory del contenuto nel server IIS</span><span class="sxs-lookup"><span data-stu-id="51b0e-107">To configure the content directory on the IIS server</span></span>**

1.  <span data-ttu-id="51b0e-108">Nel server che esegue IIS individuare la directory che si vuole usare come directory di contenuto oppure creare la directory se non esiste.</span><span class="sxs-lookup"><span data-stu-id="51b0e-108">On the server that is running IIS, locate the directory that you want to use as the content directory, or create the directory if it does not exist.</span></span> <span data-ttu-id="51b0e-109">Configurare la directory come condivisione di file standard.</span><span class="sxs-lookup"><span data-stu-id="51b0e-109">Configure this directory as a standard file share.</span></span>

2.  <span data-ttu-id="51b0e-110">Nel server in cui è in uso IIS aprire **Gestione IIS**e quindi, nel sito Web predefinito, creare una directory virtuale che corrisponda alla directory di contenuto creata nel server.</span><span class="sxs-lookup"><span data-stu-id="51b0e-110">On the server that is running IIS, open **IIS Manager**, and under the default website, create a virtual directory that corresponds to the content directory that you created on the server.</span></span> <span data-ttu-id="51b0e-111">Verificare che la **lettura** sia selezionata.</span><span class="sxs-lookup"><span data-stu-id="51b0e-111">Make sure that **Read** is checked.</span></span>

3.  <span data-ttu-id="51b0e-112">Assegnare il **contenuto**dell'alias alla directory virtuale appena creata.</span><span class="sxs-lookup"><span data-stu-id="51b0e-112">Give the newly created virtual directory the alias **Content**.</span></span>

4.  <span data-ttu-id="51b0e-113">Accettare tutte le altre impostazioni predefinite per questa directory virtuale.</span><span class="sxs-lookup"><span data-stu-id="51b0e-113">Accept all other default settings for this virtual directory.</span></span>

5.  <span data-ttu-id="51b0e-114">Configurare le autorizzazioni di file system NTFS per la directory di contenuto e le cartelle del pacchetto nella directory di contenuto usando i gruppi di sicurezza in servizi di dominio Active Directory definiti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="51b0e-114">Configure the NTFS file system permissions to the content directory and the package folders under the content directory by using the Security Groups in Active Directory Domain Services that you defined earlier.</span></span>

<span data-ttu-id="51b0e-115">**Nota**  Se si usa IIS per pubblicare i file ICO e OSD, è necessario configurare un tipo MIME per OSD = TXT; in caso contrario, IIS non servirà i file ICO e OSD ai client.</span><span class="sxs-lookup"><span data-stu-id="51b0e-115">**Note** If you are using IIS to publish the ICO and OSD files, you must configure a MIME type for OSD=TXT; otherwise, IIS will not serve the ICO and OSD files to clients.</span></span> <span data-ttu-id="51b0e-116">Se si usa IIS per pubblicare i pacchetti (file SFT), è necessario configurare un tipo MIME per SFT = Binary; in caso contrario, IIS non servirà i file SFT ai client.</span><span class="sxs-lookup"><span data-stu-id="51b0e-116">If you are using IIS to publish packages (SFT files), you must configure a MIME type for SFT=Binary; otherwise, IIS will not serve the SFT files to clients.</span></span>

 

## <span data-ttu-id="51b0e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51b0e-117">Related topics</span></span>


[<span data-ttu-id="51b0e-118">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="51b0e-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="51b0e-119">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="51b0e-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="51b0e-120">Come configurare i server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="51b0e-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="51b0e-121">Come configurare Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="51b0e-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="51b0e-122">Come configurare il file server</span><span class="sxs-lookup"><span data-stu-id="51b0e-122">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

 

 





