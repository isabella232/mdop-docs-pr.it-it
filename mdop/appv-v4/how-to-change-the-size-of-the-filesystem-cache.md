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
# Come modificare le dimensioni della cache di FileSystem


È possibile modificare le dimensioni della cache del FileSystem usando la riga di comando. Questa azione richiede un reset completo della cache e richiede diritti amministrativi.

**Per modificare le dimensioni della cache del FileSystem**

1.  Impostare il valore del registro di sistema seguente su 0 (zero):

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State

2.  Impostare il valore del registro di sistema seguente sulle dimensioni massime della cache, in MB, necessarie per contenere i pacchetti, ad esempio 8192 MB:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize

3.  Riavviare il computer.

## Argomenti correlati


[Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





