---
title: Come configurare il firewall di Windows Server 2008 per App-V
description: Come configurare il firewall di Windows Server 2008 per App-V
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817716"
---
# Come configurare il firewall di Windows Server 2008 per App-V


Con l'introduzione di Windows Server2008, il firewall e i componenti IPsec sono Stati Uniti in un unico servizio e le funzionalità di questo servizio sono state migliorate. Il nuovo servizio firewall supporta il controllo con stato in arrivo e in uscita. È inoltre possibile configurare regole firewall e criteri IPsec specifici tramite criteri di gruppo. Per altre informazioni su Windows Firewall in Windows Server2008, vedere <https://go.microsoft.com/fwlink/?LinkId=151980> .

La procedura seguente non include l'aggiunta di un'eccezione per la pubblicazione di ICO e OSD tramite SMB o HTTP/HTTPS. Tali eccezioni vengono aggiunte automaticamente in base al profilo di rete e ai ruoli installati nel firewall di Windows Server 2008.

**Nota**  Se il server di gestione è configurato per l'uso di RTSP, ripetere questa procedura per aggiungere il `sghwsvr.exe` programma come eccezione.

App-V Streaming Server richiede l'eccezione del programma `sglwdsptr.exe` per la comunicazione RTSPS. Un App-V streaming server che usa RTSP per comunicare richiede anche un'eccezione per il programma `sglwsvr.exe` .

 

**Per configurare il firewall di Windows Server2008 per App-V**

1.  Aprire **Windows Firewall con Advanced Security** Management Console tramite il pannello di controllo oppure digitando `wf.msc` la riga Esegui.

2.  Creare una nuova regola in entrata e selezionare **programma**.

3.  Selezionare il percorso del programma e passare a `sghwdsptr.exe` , che si trova per impostazione predefinita `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .

4.  Fai clic su **Avanti**.

5.  Nella pagina **azione** selezionare **Consenti la connessione**e quindi fare clic su **Avanti**.

6.  Selezionare i **profili** appropriati da applicare alla regola in ingresso.

7.  Specificare un nome e una descrizione per la regola e fare clic su **fine**.

## Argomenti correlati


[Come configurare il firewall di Windows Server 2003 per App-V](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





