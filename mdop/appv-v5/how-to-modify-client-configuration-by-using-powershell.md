---
title: Come modificare la configurazione client con PowerShell
description: Come modificare la configurazione client con PowerShell
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805271"
---
# Come modificare la configurazione client con PowerShell


Usare la procedura seguente per configurare la configurazione client App-V 5,0.

**Per modificare la configurazione client di App-V 5,0 tramite PowerShell**

1.  Per configurare le impostazioni del client tramite PowerShell, usare il cmdlet **set-AppvClientConfiguration** .

2.  Per modificare la configurazione del client, aprire un prompt dei comandi di PowerShell ed eseguire il cmdlet **set-AppvClientConfiguration** seguente con i parametri necessari. Ad esempio:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)

 

 





