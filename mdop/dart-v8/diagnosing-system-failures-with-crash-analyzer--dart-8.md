---
title: Diagnosi degli errori di sistema con Analizzatore di arresti anomali
description: Diagnosi degli errori di sistema con Analizzatore di arresti anomali
author: dansimp
ms.assetid: ce3d3186-54fb-45b2-b5ce-9bb7841db28f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: abb9d1ec99236199e0866a3b23219dd412bc9da6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824545"
---
# Diagnosi degli errori di sistema con Analizzatore di arresti anomali


L' **analizzatore crash** in Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 consente di eseguire il debug di un file di dump della memoria in un computer basato su Windows e quindi di diagnosticare gli eventuali errori del computer correlati. L' **analizzatore crash** usa gli strumenti di debug Microsoft per Windows per esaminare un file di dump della memoria per il driver che ha causato il failover del computer. È possibile eseguire l'analizzatore crash in un computer dell'utente finale o in modalità autonoma in un computer diverso da un computer dell'utente finale.

## Eseguire l'analizzatore crash in un computer con utenti finali


In genere, l' **analizzatore crash** viene eseguito dalla finestra del **set di strumenti di diagnostica e ripristino** in un computer dell'utente finale che sta verificando il problema. L' **analizzatore crash** cerca di individuare gli strumenti di debug per Windows nel computer problema. Se la finestra di dialogo percorso directory è vuota, è necessario immettere il percorso o passare al percorso degli strumenti di debug per Windows (è possibile scaricare i file da Microsoft). Devi anche specificare il percorso in cui si trovano i file di simboli.

Se sono stati inclusi gli strumenti di debug Microsoft per Windows e i file di simboli quando è stata creata l'immagine di ripristino di DaRT 8,0, gli strumenti e i file di simboli dovrebbero essere disponibili quando si esegue l' **analizzatore crash** nel computer del problema. Se non sono stati inclusi nell'immagine di ripristino di freccette o se le dimensioni del disco o i problemi di connettività di rete impediscono di ottenerli, in alternativa è possibile eseguire l'analizzatore crash in modalità autonoma in un computer diverso dal computer dell'utente finale, come descritto nella sezione seguente.

[Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-8.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a>Eseguire l'analizzatore crash in modalità autonoma in un computer diverso da un computer dell'utente finale


Anche se in genere si esegue l' **analizzatore crash** nel computer dell'utente finale che sta verificando il problema, è anche possibile eseguire l'analizzatore crash in modalità autonoma, in un computer diverso da un computer dell'utente finale. Potresti scegliere questa opzione se non hai incluso gli strumenti di debug di Windows nell'immagine di ripristino DaRT o se i problemi di connettività di rete o di dimensione del disco impediscono l'ottenimento degli strumenti di debug. In questo caso, è possibile copiare il file di dump dal computer del problema e analizzarlo in un computer in cui è installata la versione autonoma di **Crash Analyzer** , ad esempio nel computer dell'agente del supporto tecnico.

[Come eseguire Analizzatore di arresti anomali in modalità autonoma in un computer diverso quello dell'utente finale](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-8.md)

## Come assicurarsi che l'analizzatore crash possa accedere ai file di simboli


Per eseguire il debug delle applicazioni che hanno smesso di rispondere, è necessario accedere al file di simboli, che è separato dall'applicazione. Anche se i file di simboli vengono scaricati automaticamente quando si esegue l'analizzatore di crash, potrebbe verificarsi un periodo in cui il computer problema non ha accesso a Internet. Esistono diversi modi per assicurarti di avere accesso garantito ai file di simboli.

[Come verificare che Analizzatore di arresti anomali possa accedere ai file di simboli](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)

## Altre risorse per la diagnosi degli errori di sistema con Crash Analyzer


[Operazioni relative a DaRT 8.0](operations-for-dart-80-dart-8.md)

 

 





