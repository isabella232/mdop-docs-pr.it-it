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
# Come reimpostare la cache di FileSystem


La reimpostazione della cache del FileSystem non è una cosa che in genere dovrebbe essere necessaria. Tuttavia, se è necessario reimpostare completamente la cache del FileSystem, magari per scopi di risoluzione dei problemi, è possibile usare la procedura seguente. Per eseguire questa azione sono necessari diritti amministrativi.

**Per reimpostare la cache del FileSystem**

1.  Impostare il valore del registro di sistema seguente su 0 (zero):

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State

2.  Riavviare il computer.

## Argomenti correlati


[Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





