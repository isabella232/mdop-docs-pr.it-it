---
title: Come modificare le dimensioni della cache di FileSystem
description: Come modificare le dimensioni della cache di FileSystem
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818005"
---
# <span data-ttu-id="78f9b-103">Come modificare le dimensioni della cache di FileSystem</span><span class="sxs-lookup"><span data-stu-id="78f9b-103">How to Change the Size of the FileSystem Cache</span></span>


<span data-ttu-id="78f9b-104">È possibile modificare le dimensioni della cache del FileSystem usando la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="78f9b-104">You can change the size of the FileSystem cache by using the command line.</span></span> <span data-ttu-id="78f9b-105">Questa azione richiede un reset completo della cache e richiede diritti amministrativi.</span><span class="sxs-lookup"><span data-stu-id="78f9b-105">This action requires a complete reset of the cache, and it requires administrative rights.</span></span>

**<span data-ttu-id="78f9b-106">Per modificare le dimensioni della cache del FileSystem</span><span class="sxs-lookup"><span data-stu-id="78f9b-106">To change the size of the FileSystem cache</span></span>**

1.  <span data-ttu-id="78f9b-107">Impostare il valore del registro di sistema seguente su 0 (zero):</span><span class="sxs-lookup"><span data-stu-id="78f9b-107">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="78f9b-108">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="78f9b-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="78f9b-109">Impostare il valore del registro di sistema seguente sulle dimensioni massime della cache, in MB, necessarie per contenere i pacchetti, ad esempio 8192 MB:</span><span class="sxs-lookup"><span data-stu-id="78f9b-109">Set the following registry value to the maximum cache size, in MB, that is necessary to hold the packages—for example, 8192 MB:</span></span>

    <span data-ttu-id="78f9b-110">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span><span class="sxs-lookup"><span data-stu-id="78f9b-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span></span>

3.  <span data-ttu-id="78f9b-111">Riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="78f9b-111">Restart the computer.</span></span>

## <span data-ttu-id="78f9b-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="78f9b-112">Related topics</span></span>


[<span data-ttu-id="78f9b-113">Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="78f9b-113">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





