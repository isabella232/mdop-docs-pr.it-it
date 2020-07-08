---
title: Come configurare i server di gestione di Application Virtualization
description: Come configurare i server di gestione di Application Virtualization
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817845"
---
# Come configurare i server di gestione di Application Virtualization


Prima di poter eseguire il flusso delle applicazioni virtualizzate nel client Desktop Application Virtualization o nel client per Servizi Desktop remoto (in precedenza Servizi terminal), è necessario configurare l'Application Virtualization Management Server. Quando si configura il server, si sta configurando la *directory di contenuto* in cui vengono caricati e archiviati i file SFT. I file SFT contengono l'applicazione o le applicazioni virtualizzate.

**Importante**  Application Virtualization Servers Stream SFT per il client desktop e il client per i Servizi Desktop remoto usando solo protocolli RTSP o RTSPs. Il file ICO (icona) e il file OSD (Open Software Descriptor) possono essere configurati in streaming da un file o un server HTTP diverso.

 

**Per configurare l'Application Virtualization Management Server**

1.  Completare la procedura seguente:

    [Come installare il server di gestione di Application Virtualization](how-to-install-application-virtualization-management-server.md)

    **Nota**  Durante la procedura di installazione, specificare la posizione della directory \\Content nella schermata **percorso contenuto** .

     

2.  Passare al percorso specificato per la directory \\Content e, se necessario, creare la directory.

3.  Quando viene creata la directory di contenuto, configurare la directory come condivisione di file standard.

## Argomenti correlati


[Scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Requisiti di sistema di Application Virtualization](application-virtualization-system-requirements.md)

[Scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario.md)

[Come configurare i server per la distribuzione basata su server](how-to-configure-servers-for-server-based-deployment.md)

 

 





