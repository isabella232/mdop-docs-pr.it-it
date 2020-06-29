---
title: Come configurare il client per la modalità di operazioni senza connessione
description: Come configurare il client per la modalità di operazioni senza connessione
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817816"
---
# Come configurare il client per la modalità di operazioni senza connessione


La modalità operativa disconnessa consente al client Desktop Application Virtualization (App-V) o al client Application Virtualization (App-V) per Servizi Desktop remoto (in precedenza Servizi terminal) di eseguire applicazioni archiviate nella cache del file System del client quando il client non riesce a connettersi al server di gestione di App-V.

**Importante**  In un'organizzazione di grandi dimensioni in cui più server Host sessione Desktop remoto (in precedenza Terminal Server) sono collegati in una farm per supportare molti utenti, l'uso di un'unica App-V Management Server per supportare la farm rappresenta un singolo punto di errore. Per ottenere una disponibilità elevata per supportare la farm host di RDSession, è consigliabile collegare due o più server di gestione di App-V per usare lo stesso database.

 

**Per abilitare la modalità di operazione disconnessa**

-   Impostare il valore della chiave del registro di sistema seguente uguale a 1 per abilitare la modalità di operazione disconnessa:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

**Per impostare un limite di tempo per l'uso della modalità di operazione disconnessa**

1.  Impostare il valore della chiave del registro di sistema seguente su 1:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

2.  Impostare il valore della chiave del registro di sistema seguente sul numero di minuti per cui si vuole limitare la modalità di operazione disconnessa. L'intervallo di valori valido è 1-999999. Il valore predefinito è 90 giorni o 129.600 minuti.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes

**Per configurare il client per Servizi Desktop remoto per la modalità di operazione disconnessa**

1.  Impostare il valore della chiave del registro di sistema seguente su 1 per abilitare la modalità di operazione disconnessa:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

2.  Impostare il valore della chiave del registro di sistema seguente su 0 (zero) per consentire l'utilizzo illimitato della modalità di operazione disconnessa:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

3.  Assicurarsi che tutti i pacchetti vengano precaricati nella cache per migliorare le prestazioni.

## Argomenti correlati


[Modalità di operazioni senza connessione](disconnected-operation-mode.md)

[Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





