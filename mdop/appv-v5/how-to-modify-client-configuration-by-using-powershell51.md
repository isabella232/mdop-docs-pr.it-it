---
title: Come modificare la configurazione client con PowerShell
description: Come modificare la configurazione client con PowerShell
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805259"
---
# Come modificare la configurazione client con PowerShell


Usare la procedura seguente per configurare la configurazione client App-V 5,1.

**Per modificare la configurazione client di App-V 5,1 tramite PowerShell**

1.  Per configurare le impostazioni del client tramite PowerShell, usare il cmdlet **set-AppvClientConfiguration** . Per altre informazioni sull'installazione di PowerShell e un elenco di cmdlet, vedere [come caricare i cmdlet di PowerShell e ottenere la guida per i cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).

2.  Per modificare la configurazione del client, aprire un prompt dei comandi di PowerShell ed eseguire il cmdlet **set-AppvClientConfiguration** seguente con i parametri necessari. Ad esempio:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)

 

 





