---
title: Come configurare il firewall di Windows Server 2003 per App-V
description: Come configurare il firewall di Windows Server 2003 per App-V
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817726"
---
# Come configurare il firewall di Windows Server 2003 per App-V


Usare la procedura seguente per configurare il firewall di WindowsServer 2003 per App-V.

**Per configurare il firewall di WindowsServer 2003 per App-V**

1.  Nel **Pannello di controllo**aprire **Windows Firewall**.

    **Nota**  Se il server non è stato configurato per l'esecuzione del servizio firewall prima di questo passaggio, verrà richiesto di avviare il servizio firewall.

     

2.  Se i file ICO e OSD vengono pubblicati tramite SMB, verificare che la **condivisione di file e stampanti** sia abilitata nella scheda **eccezioni** .

    **Nota**  Se i file ICO e OSD vengono pubblicati tramite HTTP/HTTPS nel server di gestione, potrebbe essere necessario aggiungere un'eccezione per HTTP o HTTPS. Se il server IIS che ospita i file ICO e OSD è ospitato in un computer separato dal server di gestione, è necessario aggiungere l'eccezione a tale computer. Per ottimizzare le prestazioni, è consigliabile ospitare i file ICO e OSD in un server separato dal server di gestione.

     

3.  Aggiungere un'eccezione per `sghwdsptr.exe` il programma, ovvero l'eseguibile del servizio server di gestione. Il percorso predefinito di questo eseguibile è `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .

    **Nota**  Se il server di gestione USA RTSP per la comunicazione, è necessario aggiungere anche un'eccezione per il programma `sghwsvr.exe` .

    App-V Streaming Server richiede un'eccezione di programma `sglwdsptr.exe` per la comunicazione RTSPS. L'App-V streaming server che usa RTSP per comunicare richiede anche un'eccezione per il programma `sglwsvr.exe` .

     

4.  Verificare che l'ambito appropriato sia configurato per ogni eccezione. Per ridurre il rischio, rimuovere qualsiasi computer e limitare rigorosamente gli indirizzi IP a cui il server risponderà.

## Argomenti correlati


[Come configurare il firewall di Windows Server 2008 per App-V](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 





