---
title: Come consentire solo agli amministratori di pubblicare i pacchetti con ESD
description: Come consentire solo agli amministratori di pubblicare i pacchetti con ESD
author: dansimp
ms.assetid: 03367b26-83d5-4299-ad52-b9177b9cf9a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 341e86ca806c5acc736c78cf8072aab6fb4286df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805481"
---
# Come consentire solo agli amministratori di pubblicare i pacchetti con ESD


A partire da App-V 5,0 SP3 puoi configurare il client App-V in modo che solo gli amministratori (non gli utenti finali) possano pubblicare o annullare la pubblicazione di pacchetti. Nelle versioni precedenti di App-V non è stato possibile impedire agli utenti finali di eseguire queste attività.

**Per consentire solo agli amministratori di pubblicare o annullare la pubblicazione di pacchetti**

1.  Passare al nodo oggetto Criteri di gruppo seguente:

    **Configurazione &gt; computer Criteri &gt; amministrativi modelli &gt; &gt; di sistema App-V &gt; Publishing**.

2.  Abilitare l'impostazione Richiedi i criteri **di gruppo pubblica come amministratore** .

    Per usare in alternativa PowerShell per impostare questo elemento, vedere [come gestire i pacchetti App-V 5,0 in uso in un computer autonomo usando PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





