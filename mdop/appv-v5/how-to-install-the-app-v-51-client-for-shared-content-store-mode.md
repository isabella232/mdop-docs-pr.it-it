---
title: Come installare il client App-V 5.1 per la modalità SCS (Shared Content Store)
description: Come installare il client App-V 5.1 per la modalità SCS (Shared Content Store)
author: dansimp
ms.assetid: 6f3ecb1b-b5b5-4ae0-8de9-b4ffdfd2c216
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7ce8114a44762180bf9bb0240913dca50c55d31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805439"
---
# Come installare il client App-V 5.1 per la modalità SCS (Shared Content Store)


Usare la procedura seguente per installare il client di Microsoft Application Virtualization (App-V) 5,1 in modo che usi la modalità SCS (Shared Content Store) App-V 5,1. Devi verificare che tutti i prerequisiti necessari siano installati nel computer in cui intendi installare. Usare il collegamento seguente per visualizzare i [prerequisiti di App-V 5,1](app-v-51-prerequisites.md).

**Nota**  Prima di eseguire questa procedura, se necessario, disinstallare le versioni esistenti del client App-V 5,1.

 

Per altre informazioni sulla modalità SCS, vedere [archivio contenuto condiviso in Microsoft App-V 5,0-dietro le quinte](https://go.microsoft.com/fwlink/?LinkId=316879) ( https://go.microsoft.com/fwlink/?LinkId=316879) .

**Installare e configurare il client App-V 5,1 per la modalità SCS**

1.  Copiare i file di installazione del client App-V 5,1 nel computer in cui verrà installato. Aprire una riga di comando e dalla directory in cui vengono salvati i file di installazione digitare una delle opzioni seguenti, a seconda della versione del client che si sta installando:

    -   Per installare la versione RDS del tipo di client App-V 5,1: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**

    -   Per installare la versione standard del tipo di client App-V 5,1: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**

        **Importante**  È necessario eseguire un'installazione invisibile all'utente o l'installazione avrà esito negativo.

         

2.  Dopo aver completato l'installazione, è possibile distribuire pacchetti al computer che ha eseguito il client e tutti i contenuti del pacchetto verranno trasmessi in streaming nella rete.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Distribuzione di App-V 5.1 Sequencer e del client](deploying-the-app-v-51-sequencer-and-client.md)

 

 





