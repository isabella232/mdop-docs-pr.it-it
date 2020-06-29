---
title: Come consentire solo agli amministratori di pubblicare i pacchetti con ESD
description: Come consentire solo agli amministratori di pubblicare i pacchetti con ESD
author: dansimp
ms.assetid: bbc9fda2-fc09-4d72-8d9a-e83d2fcfe234
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22de7f62f540ceff274862c3f16b1f89d9459093
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805469"
---
# Come consentire solo agli amministratori di pubblicare i pacchetti con ESD


A partire da App-V 5,0 SP3 puoi configurare il client App-V in modo che solo gli amministratori (non gli utenti finali) possano pubblicare o annullare la pubblicazione di pacchetti. Nelle versioni precedenti di App-V non è stato possibile impedire agli utenti finali di eseguire queste attività.

**Per consentire solo agli amministratori di pubblicare o annullare la pubblicazione di pacchetti**

1.  Passare al nodo oggetto Criteri di gruppo seguente:

    **Configurazione &gt; computer Criteri &gt; amministrativi modelli &gt; &gt; di sistema App-V &gt; Publishing**.

2.  Abilitare l'impostazione Richiedi i criteri **di gruppo pubblica come amministratore** .

    Per usare in alternativa PowerShell per impostare questo elemento, vedere [come gestire i pacchetti App-V 5,1 in uso in un computer autonomo usando PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





