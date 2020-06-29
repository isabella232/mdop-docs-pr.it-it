---
title: Come reimpostare la cache di FileSystem
description: Come reimpostare la cache di FileSystem
author: dansimp
ms.assetid: 7777259d-8c21-4c06-9384-9599b69f9828
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 680634d98f8aac048af605c62029a0ee6b20af03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816715"
---
# <span data-ttu-id="8f377-103">Come reimpostare la cache di FileSystem</span><span class="sxs-lookup"><span data-stu-id="8f377-103">How to Reset the FileSystem Cache</span></span>


<span data-ttu-id="8f377-104">La reimpostazione della cache del FileSystem non è una cosa che in genere dovrebbe essere necessaria.</span><span class="sxs-lookup"><span data-stu-id="8f377-104">Resetting the FileSystem cache is not something that should usually be necessary.</span></span> <span data-ttu-id="8f377-105">Tuttavia, se è necessario reimpostare completamente la cache del FileSystem, magari per scopi di risoluzione dei problemi, è possibile usare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="8f377-105">However if you need to completely reset the FileSystem cache, perhaps for troubleshooting purposes, you can use the following procedure.</span></span> <span data-ttu-id="8f377-106">Per eseguire questa azione sono necessari diritti amministrativi.</span><span class="sxs-lookup"><span data-stu-id="8f377-106">Administrative rights are required to perform this action.</span></span>

**<span data-ttu-id="8f377-107">Per reimpostare la cache del FileSystem</span><span class="sxs-lookup"><span data-stu-id="8f377-107">To reset the FileSystem cache</span></span>**

1.  <span data-ttu-id="8f377-108">Impostare il valore del registro di sistema seguente su 0 (zero):</span><span class="sxs-lookup"><span data-stu-id="8f377-108">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="8f377-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="8f377-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="8f377-110">Riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="8f377-110">Restart the computer.</span></span>

## <span data-ttu-id="8f377-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f377-111">Related topics</span></span>


[<span data-ttu-id="8f377-112">Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="8f377-112">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





