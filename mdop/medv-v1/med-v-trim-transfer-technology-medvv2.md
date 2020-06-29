---
title: Tecnologia TrimTransfer di MED-V
description: Tecnologia TrimTransfer di MED-V
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826186"
---
# <span data-ttu-id="93bd9-103">Tecnologia TrimTransfer di MED-V</span><span class="sxs-lookup"><span data-stu-id="93bd9-103">MED-V Trim Transfer Technology</span></span>


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


<span data-ttu-id="93bd9-104">La tecnologia di deduplicazione Advanced Trim Transfer MED-V consente di velocizzare il download delle immagini delle macchine virtuali iniziali e aggiornate tramite la rete LAN o WAN, riducendo così la larghezza di banda necessaria per il trasporto di una macchina virtuale dell'area di lavoro MED-V a più utenti finali.</span><span class="sxs-lookup"><span data-stu-id="93bd9-104">The MED-V advanced Trim Transfer de-duplication technology accelerates the download of initial and updated virtual machine images over the LAN or WAN, thereby reducing the network bandwidth needed to transport a MED-V workspace virtual machine to multiple end users.</span></span>

<span data-ttu-id="93bd9-105">Questa tecnologia rivoluzionaria usa i dati locali esistenti per creare l'immagine della macchina virtuale, sfruttando il fatto che in molti casi, la maggior parte della macchina virtuale, ad esempio i file di sistema e applicazione, esiste già nel disco dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="93bd9-105">This breakthrough technology uses existing local data to build the virtual machine image, leveraging the fact that in many cases, much of the virtual machine (for example, system and application files) already exists on the end user's disk.</span></span> <span data-ttu-id="93bd9-106">Ad esempio, se una macchina virtuale contenente WindowsXP viene recapitata a un client che gestisce una copia locale di WindowsXP, MED-V rimuoverà automaticamente gli elementi di WindowsXP ridondanti dal trasferimento.</span><span class="sxs-lookup"><span data-stu-id="93bd9-106">For example, if a virtual machine containing WindowsXP is delivered to a client running a local copy of WindowsXP, MED-V will automatically remove the redundant WindowsXP elements from the transfer.</span></span> <span data-ttu-id="93bd9-107">Per garantire un'area di lavoro valida e funzionale, il client MED-V verifica in modo crittografico l'integrità dei dati locali prima che venga utilizzata, garantendo che i blocchi di dati locali siano identici per bit a quelli nell'immagine della macchina virtuale desiderata.</span><span class="sxs-lookup"><span data-stu-id="93bd9-107">To ensure a valid and functional workspace, the MED-V client cryptographically verifies the integrity of local data before it is utilized, guaranteeing that the local blocks of data are absolutely bit-by-bit identical to those in the desired virtual machine image.</span></span> <span data-ttu-id="93bd9-108">I blocchi che non corrispondono non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="93bd9-108">Blocks that do not match are not used.</span></span>

<span data-ttu-id="93bd9-109">Il processo è efficiente per la larghezza di banda e trasparente e i trasferimenti vengono eseguiti in background, usando risorse di rete e CPU inutilizzate.</span><span class="sxs-lookup"><span data-stu-id="93bd9-109">The process is bandwidth-efficient and transparent, and transfers run in the background, utilizing unused network and CPU resources.</span></span>

<span data-ttu-id="93bd9-110">Quando si esegue l'aggiornamento a una nuova versione di immagine, ad esempio quando gli amministratori desiderano distribuire una nuova applicazione o patch, vengono scaricati solo gli elementi che sono stati modificati ("Delta") e non l'intera macchina virtuale, riducendo in modo significativo la larghezza di banda e il tempo di consegna della rete necessari.</span><span class="sxs-lookup"><span data-stu-id="93bd9-110">When updating to a new image version (for example, when administrators want to distribute a new application or patch), only the elements that have changed ("deltas") are downloaded, and not the entire virtual machine, significantly reducing the required network bandwidth and delivery time.</span></span>

<span data-ttu-id="93bd9-111">Puoi configurare le cartelle indicizzate nell'host come parte del protocollo di trasferimento trim, in base al sistema operativo host.</span><span class="sxs-lookup"><span data-stu-id="93bd9-111">You can configure which folders are indexed on the host as part of the Trim Transfer protocol, based on the host operating system.</span></span> <span data-ttu-id="93bd9-112">Queste impostazioni sono configurate nel file *ClientSettings.xml* , che si trova nella cartella **Servers\\Configuration Server\\** .</span><span class="sxs-lookup"><span data-stu-id="93bd9-112">These settings are configured in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="93bd9-113">Quando si applicano nuove impostazioni, il servizio deve essere riavviato.</span><span class="sxs-lookup"><span data-stu-id="93bd9-113">When applying new settings, the service must be restarted.</span></span>

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 





