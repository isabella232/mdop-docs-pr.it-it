---
title: Configurazione di MED-V per le reti remote
description: Configurazione di MED-V per le reti remote
author: dansimp
ms.assetid: 4d2f0081-622f-4a6f-8d73-f8c2108036e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328376046ee5213f3d5bb09be7adf8c81f8508b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826725"
---
# <span data-ttu-id="0b1c7-103">Configurazione di MED-V per le reti remote</span><span class="sxs-lookup"><span data-stu-id="0b1c7-103">Configuring MED-V for Remote Networks</span></span>


<span data-ttu-id="0b1c7-104">È possibile configurare MED-V in modo che funzioni all'interno di una rete, in remoto o sia dall'interno della rete che da remoto.</span><span class="sxs-lookup"><span data-stu-id="0b1c7-104">You can configure MED-V to work from inside a network, remotely, or both from inside the network and remotely.</span></span>

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**<span data-ttu-id="0b1c7-105">Per configurare MED-V per l'utilizzo all'interno di una rete</span><span class="sxs-lookup"><span data-stu-id="0b1c7-105">To configure MED-V to work from inside a network</span></span>**

-   <span data-ttu-id="0b1c7-106">Configurare un server MED-V e una distribuzione di immagini all'interno della rete.</span><span class="sxs-lookup"><span data-stu-id="0b1c7-106">Configure a MED-V server and image distribution inside the network.</span></span>

**<span data-ttu-id="0b1c7-107">Per configurare MED-V per il lavoro in remoto</span><span class="sxs-lookup"><span data-stu-id="0b1c7-107">To configure MED-V to work remotely</span></span>**

1.  <span data-ttu-id="0b1c7-108">Configurare un server MED-V e un server di distribuzione delle immagini accessibile da Internet.</span><span class="sxs-lookup"><span data-stu-id="0b1c7-108">Configure a MED-V server and an image distribution server that are accessible from the Internet.</span></span>

2.  <span data-ttu-id="0b1c7-109">Se necessario, configurare una rete perimetrale (detta anche DMZ) come proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="0b1c7-109">If needed, configure a perimeter network (also called a DMZ) reverse proxy.</span></span>

3.  <span data-ttu-id="0b1c7-110">Impostare il metodo di autenticazione, nel file *ClientSettings.xml* , che si trova nella cartella **Servers\\Configuration Server\\** .</span><span class="sxs-lookup"><span data-stu-id="0b1c7-110">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

**<span data-ttu-id="0b1c7-111">Per configurare MED-V in modo che funzioni sia dall'interno di una rete che da remoto</span><span class="sxs-lookup"><span data-stu-id="0b1c7-111">To configure MED-V to work both from inside a network and remotely</span></span>**

1.  <span data-ttu-id="0b1c7-112">Configurare un server MED-V e un server di distribuzione delle immagini all'interno della rete.</span><span class="sxs-lookup"><span data-stu-id="0b1c7-112">Configure a MED-V server and image distribution server inside the network.</span></span>

2.  <span data-ttu-id="0b1c7-113">Verificare che i server siano accessibili da Internet.</span><span class="sxs-lookup"><span data-stu-id="0b1c7-113">Ensure that the servers are accessible from the Internet.</span></span>

3.  <span data-ttu-id="0b1c7-114">Configurare la risoluzione DNS in modo che quando il client tenti di connettersi a un server, si connetta automaticamente al server corretto (all'interno della rete o tramite Internet) in base alla posizione del client.</span><span class="sxs-lookup"><span data-stu-id="0b1c7-114">Configure the DNS resolution so that when the client attempts to connect to a server, it automatically connects to the correct server (within the network or over the Internet) based on the client location.</span></span>

4.  <span data-ttu-id="0b1c7-115">Se necessario, configurare un proxy inverso della rete perimetrale.</span><span class="sxs-lookup"><span data-stu-id="0b1c7-115">If needed, configure a perimeter network reverse proxy.</span></span>

5.  <span data-ttu-id="0b1c7-116">Impostare il metodo di autenticazione, nel file *ClientSettings.xml* , che si trova nella cartella **Servers\\Configuration Server\\** .</span><span class="sxs-lookup"><span data-stu-id="0b1c7-116">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="0b1c7-117">**Nota**  Quando si applicano nuove impostazioni, il servizio deve essere riavviato.</span><span class="sxs-lookup"><span data-stu-id="0b1c7-117">**Note** When applying new settings, the service must be restarted.</span></span>

 

-   <span data-ttu-id="0b1c7-118">È possibile modificare lo schema di autenticazione di IIS in una delle opzioni seguenti: BASIC, DIGEST, NTLM o NEGOTIATe.</span><span class="sxs-lookup"><span data-stu-id="0b1c7-118">You can change the IIS authentication scheme to one of the following: BASIC, DIGEST, NTLM, or NEGOTIATE.</span></span> <span data-ttu-id="0b1c7-119">Il valore predefinito è NEGOTIATe e usa la voce seguente:</span><span class="sxs-lookup"><span data-stu-id="0b1c7-119">The default is NEGOTIATE and uses the following entry:</span></span>

    ```xml
    <ImageDistribution>
    <!-- The authentication used for image download. Basic and digest authentication should be used only under SSL.-->
       <!-- The line below can be one of the following: -->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_BASIC</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_DIGEST</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NTLM</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME-->
       <Authentication type="Kidaro.Foundation.Bits.BG_AUTH_SCHEME">
          <BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME>
       </Authentication>
    </ImageDistribution>
    ```

## <span data-ttu-id="0b1c7-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b1c7-120">Related topics</span></span>


[<span data-ttu-id="0b1c7-121">Progettazione e pianificazione dell'infrastruttura MED-V</span><span class="sxs-lookup"><span data-stu-id="0b1c7-121">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





