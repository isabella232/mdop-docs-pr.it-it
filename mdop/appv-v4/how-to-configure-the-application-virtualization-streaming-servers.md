---
title: Come configurare Application Virtualization Streaming Server
description: Come configurare Application Virtualization Streaming Server
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817825"
---
# Come configurare Application Virtualization Streaming Server


Prima che le applicazioni virtuali possano essere trasmesse al client Desktop Application Virtualization o al client per Servizi Desktop remoto (in precedenza Servizi terminal), è necessario configurare i server di streaming Application Virtualization. Quando configuri i server, stai configurando la *directory di contenuto* in cui vengono caricati e archiviati i file SFT. I file SFT contengono l'applicazione virtuale (o le applicazioni).

**Importante**  Application Virtualization Servers Stream SFT per il client desktop e il client per i Servizi Desktop remoto usando solo protocolli RTSP o RTSPs. Il file ICO (icona) e il file OSD (Open Software Descriptor) possono essere configurati in streaming da un file o un server HTTP diverso.

 

**Per configurare i server di streaming Application Virtualization**

1.  Completare la procedura di installazione per Application Virtualization Streaming Server. Durante la procedura di installazione, specificare la posizione della directory \\Content nella schermata **percorso contenuto** .

2.  Passare al percorso specificato per la directory \\Content e, se necessario, creare la directory.

3.  Quando viene creata la directory di contenuto, configurare la directory come condivisione di file standard.

4.  Configurare le autorizzazioni di file system NTFS per la directory di contenuto e le cartelle del pacchetto nella directory di contenuto. È consigliabile usare i gruppi di sicurezza in servizi di dominio Active Directory che definiscono gli utenti che possono accedere a ogni applicazione.

## Argomenti correlati


[Scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario.md)

[Come configurare i server di gestione di Application Virtualization](how-to-configure-the-application-virtualization-management-servers.md)

[Come configurare il file server](how-to-configure-the-file-server.md)

[Come configurare il server per IIS](how-to-configure-the-server-for-iis.md)

 

 





