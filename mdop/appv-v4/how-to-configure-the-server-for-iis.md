---
title: Come configurare il server per IIS
description: Come configurare il server per IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817745"
---
# Come configurare il server per IIS


Prima che le applicazioni virtuali possano essere trasmesse al client Desktop Application Virtualization e al client per Servizi Desktop remoto (in precedenza Servizi terminal), è necessario configurare i server IIS. Quando configuri i server, stai configurando la directory di contenuto in cui vengono caricati e archiviati i file SFT. I file SFT contengono l'applicazione virtuale (o le applicazioni).

**Per configurare la directory del contenuto nel server IIS**

1.  Nel server che esegue IIS individuare la directory che si vuole usare come directory di contenuto oppure creare la directory se non esiste. Configurare la directory come condivisione di file standard.

2.  Nel server in cui è in uso IIS aprire **Gestione IIS**e quindi, nel sito Web predefinito, creare una directory virtuale che corrisponda alla directory di contenuto creata nel server. Verificare che la **lettura** sia selezionata.

3.  Assegnare il **contenuto**dell'alias alla directory virtuale appena creata.

4.  Accettare tutte le altre impostazioni predefinite per questa directory virtuale.

5.  Configurare le autorizzazioni di file system NTFS per la directory di contenuto e le cartelle del pacchetto nella directory di contenuto usando i gruppi di sicurezza in servizi di dominio Active Directory definiti in precedenza.

**Nota**  Se si usa IIS per pubblicare i file ICO e OSD, è necessario configurare un tipo MIME per OSD = TXT; in caso contrario, IIS non servirà i file ICO e OSD ai client. Se si usa IIS per pubblicare i pacchetti (file SFT), è necessario configurare un tipo MIME per SFT = Binary; in caso contrario, IIS non servirà i file SFT ai client.

 

## Argomenti correlati


[Scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario.md)

[Come configurare i server di gestione di Application Virtualization](how-to-configure-the-application-virtualization-management-servers.md)

[Come configurare Application Virtualization Streaming Server](how-to-configure-the-application-virtualization-streaming-servers.md)

[Come configurare il file server](how-to-configure-the-file-server.md)

 

 





