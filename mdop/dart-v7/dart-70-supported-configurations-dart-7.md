---
title: Configurazioni supportate di DaRT 7.0
description: Configurazioni supportate di DaRT 7.0
author: dansimp
ms.assetid: e9ee87b0-3254-4625-b178-17b2f5b8f8c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b074a061c402f86769e42d873e0119ac54080c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804419"
---
# <span data-ttu-id="47b04-103">Configurazioni supportate di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="47b04-103">DaRT 7.0 Supported Configurations</span></span>


<span data-ttu-id="47b04-104">L'ambiente può già soddisfare i requisiti di configurazione forniti in questo articolo in modo da poter installare ed eseguire Microsoft Diagnostics and Recovery Toolset (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="47b04-104">Your environment may already meet the configuration requirements provided here so that you can install and run Microsoft Diagnostics and Recovery Toolset (DaRT)7.</span></span> <span data-ttu-id="47b04-105">Questi includono i requisiti seguenti per l'immagine di ripristino e lo spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="47b04-105">These include the following recovery image and disk space requirements.</span></span>

## <span data-ttu-id="47b04-106">Requisiti per l'immagine di ripristino DaRT 7</span><span class="sxs-lookup"><span data-stu-id="47b04-106">DaRT 7 Recovery Image Requirements</span></span>


<span data-ttu-id="47b04-107">Non è supportata la creazione di immagini di ripristino multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="47b04-107">No cross-platform recovery image creation is supported.</span></span> <span data-ttu-id="47b04-108">Nella tabella seguente viene specificato il tipo di immagine di ripristino che è necessario creare e distribuire nell'organizzazione:</span><span class="sxs-lookup"><span data-stu-id="47b04-108">The following table specifies the kind of recovery image that you should create and deploy in your enterprise:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47b04-109">Piattaforma e versione DaRT</span><span class="sxs-lookup"><span data-stu-id="47b04-109">Platform and DaRT Version</span></span></th>
<th align="left"><span data-ttu-id="47b04-110">Requisiti per l'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="47b04-110">Recovery Image Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47b04-111">64 bit DaRT 7,0</span><span class="sxs-lookup"><span data-stu-id="47b04-111">64-Bit DaRT 7.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="47b04-112">Creare e usare un'immagine di ripristino delle freccette di 64 bit.</span><span class="sxs-lookup"><span data-stu-id="47b04-112">Create and use a 64-Bit DaRT recovery image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47b04-113">32 bit DaRT 7,0</span><span class="sxs-lookup"><span data-stu-id="47b04-113">32-Bit DaRT 7.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="47b04-114">Creare e usare un'immagine di ripristino delle freccette di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="47b04-114">Create and use a 32-Bit DaRT recovery image.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="47b04-115">Requisiti per i computer degli utenti finali di DaRT 7</span><span class="sxs-lookup"><span data-stu-id="47b04-115">DaRT 7 End-user Computer Requirements</span></span>


<span data-ttu-id="47b04-116">La finestra del **set di strumenti di diagnostica e ripristino** in DART richiede che il computer di destinazione usi uno dei sistemi operativi seguenti insieme alla quantità specificata di memoria di sistema disponibile per DART:</span><span class="sxs-lookup"><span data-stu-id="47b04-116">The **Diagnostics and Recovery Toolset** window in DaRT requires that the destination computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47b04-117">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="47b04-117">Operating System</span></span></th>
<th align="left"><span data-ttu-id="47b04-118">Requisiti di sistema per DaRT</span><span class="sxs-lookup"><span data-stu-id="47b04-118">System Requirements for DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47b04-119">Windows7 64 bit (2GB)</span><span class="sxs-lookup"><span data-stu-id="47b04-119">Windows7 64-Bit (2GB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="47b04-120">2,5 GB di memoria di sistema</span><span class="sxs-lookup"><span data-stu-id="47b04-120">2.5GB of system memory</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47b04-121">Windows7 32 bit (1GB)</span><span class="sxs-lookup"><span data-stu-id="47b04-121">Windows7 32-Bit (1GB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="47b04-122">1.5 GB di memoria di sistema</span><span class="sxs-lookup"><span data-stu-id="47b04-122">1.5GB of system memory</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47b04-123">Windows Server2008R2 (512MB)</span><span class="sxs-lookup"><span data-stu-id="47b04-123">Windows Server2008R2 (512MB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="47b04-124">1GB di memoria di sistema</span><span class="sxs-lookup"><span data-stu-id="47b04-124">1GB of system memory</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="47b04-125">DaRT offre anche i requisiti hardware minimi seguenti:</span><span class="sxs-lookup"><span data-stu-id="47b04-125">DaRT also has the following minimal hardware requirements:</span></span>

-   <span data-ttu-id="47b04-126">Un'unità CD o DVD o una porta USB</span><span class="sxs-lookup"><span data-stu-id="47b04-126">A CD or DVD drive or a USB port</span></span>

    <span data-ttu-id="47b04-127">Questa operazione è obbligatoria se si distribuisce un dardo nell'organizzazione usando un CD, un DVD o un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="47b04-127">This is required if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

-   <span data-ttu-id="47b04-128">Supporto del BIOS per avviare il computer da un CD o DVD, da un'unità flash USB o da una partizione remota o di ripristino</span><span class="sxs-lookup"><span data-stu-id="47b04-128">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition</span></span>

## <span data-ttu-id="47b04-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47b04-129">Related topics</span></span>


[<span data-ttu-id="47b04-130">Pianificazione della distribuzione di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="47b04-130">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





