---
title: Come configurare il file server
description: Come configurare il file server
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817785"
---
# Come configurare il file server


È possibile usare la procedura seguente per configurare un computer locale usato come condivisione di file e le applicazioni di flussi per il client Desktop Application Virtualization e il client per Servizi Desktop remoto (in precedenza Servizi terminal). Questo scenario viene usato quando non si vuole aggiungere un'ulteriore infrastruttura server all'ambiente hardware esistente.

Se si usa un Application Virtualization Management Server come punto di distribuzione per la condivisione file installata negli uffici locali, è necessario configurare questo server prima che le applicazioni virtuali possano essere trasmesse ai computer usati come condivisioni file. Quando si configurano i server e le condivisioni file, si configura la directory di contenuto in cui vengono caricati e archiviati i file SFT. I file SFT contengono l'applicazione virtuale (o le applicazioni).

**Importante**  Affinché le applicazioni vengano trasmesse correttamente al client Desktop Application Virtualization e al client per Servizi Desktop remoto, i flussi di file SFT dalla directory di contenuto nel server in cui è archiviata l'applicazione virtuale; il file ICO (icona) e il file OSD (Open Software Descriptor) possono essere configurati in streaming da un server diverso.

 

**Per configurare l'Application Virtualization file server**

1.  Completare la procedura di installazione seguente per configurare il server usato come punto di distribuzione:

    [Come installare il server di gestione di Application Virtualization](how-to-install-application-virtualization-management-server.md)

    **Nota**  Durante la procedura di installazione, specificare la posizione della directory \\Content nella schermata **percorso contenuto** .

     

2.  Creare una directory \\Content, che corrisponde alla directory specificata durante l'installazione del server, in ogni computer in uso come condivisione file.

    **Importante**  Configurare i client Desktop Application Virtualization per eseguire il flusso delle applicazioni dal computer in uso come condivisione file anziché da un server di virtualizzazione dell'applicazione o da un server IIS.

     

3.  Quando viene creata la directory \\Content, configurare la directory come condivisione file standard.

## Argomenti correlati


[Scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario.md)

[Come configurare i server di gestione di Application Virtualization](how-to-configure-the-application-virtualization-management-servers.md)

[Come configurare Application Virtualization Streaming Server](how-to-configure-the-application-virtualization-streaming-servers.md)

[Come configurare il server per IIS](how-to-configure-the-server-for-iis.md)

 

 





