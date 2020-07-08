---
title: Diagnosi degli errori di sistema con Analizzatore di arresti anomali
description: Diagnosi degli errori di sistema con Analizzatore di arresti anomali
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823466"
---
# Diagnosi degli errori di sistema con Analizzatore di arresti anomali


L'analizzatore crash in Microsoft Diagnostics and Recovery Toolset (DaRT) 7 consente di eseguire il debug di un file di dump di arresto anomalo in un computer basato su Windows e quindi di diagnosticare gli eventuali errori relativi al computer. L'analizzatore crash usa gli strumenti di debug Microsoft per Windows per esaminare un file di dump di arresto anomalo per il driver che ha causato il failover del computer.

## Eseguire l'analizzatore crash in un computer dell'utente finale


In genere, l'analizzatore crash viene eseguito dalla finestra del set di strumenti di diagnostica e ripristino in un computer dell'utente finale che presenta problemi. L'analizzatore crash cerca di individuare gli strumenti di debug per Windows nel computer problema. Se la finestra di dialogo percorso directory è vuota, è necessario immettere la posizione o passare al percorso degli strumenti di debug per Windows (è possibile scaricare i file da Microsoft). Devi anche specificare il percorso in cui si trovano i file di simboli.

Se sono stati inclusi gli strumenti di debug Microsoft per Windows e i file di simboli quando è stata creata l'immagine di ripristino di DaRT, dovrebbero essere disponibili quando si esegue l'analizzatore crash nel computer del problema.

[Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## Eseguire l'analizzatore crash in modalità autonoma in un computer diverso da un computer dell'utente finale


L'analizzatore crash cerca di individuare gli strumenti di debug per Windows nel computer problema. Se la finestra di dialogo percorso directory è vuota, è necessario immettere la posizione o passare al percorso degli strumenti di debug per Windows (è possibile scaricare i file da Microsoft). Devi anche specificare il percorso in cui si trovano i file di simboli.

Se non sono stati inclusi gli strumenti di debug Microsoft per Windows e i file di simboli quando è stata creata l'immagine di ripristino di freccette o se i problemi di connettività di rete o le dimensioni del disco impediscono di ottenerli, è possibile copiare il file di dump dal computer del problema e analizzarlo in un computer in cui è installata la versione autonoma di analizzatore crash. , ad esempio un computer dell'amministratore dell'helpdesk.

[Come eseguire Analizzatore di arresti anomali in modalità autonoma in un computer diverso quello dell'utente finale](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## Verificare che Crash Analyzer possa accedere ai file di simboli


In genere, le informazioni di debug sono archiviate in un file di simboli separato dall'eseguibile. È necessario avere accesso alle informazioni sul simbolo quando si effettua il debug di un'applicazione che ha smesso di rispondere, ad esempio se è stata arrestata.

I file di simboli vengono scaricati automaticamente quando si esegue analizzatore crash. Se il computer non dispone di una connessione Internet o se la rete richiede che il computer acceda a un server proxy HTTP, non è possibile scaricare i file di simboli.

[Come verificare che Analizzatore di arresti anomali possa accedere ai file di simboli](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## Altre risorse per la diagnosi degli errori di sistema con Crash Analyzer


[Operazioni relative a DaRT 7.0](operations-for-dart-70-new-ia.md)

 

 





