---
title: Come creare la directory radice del pacchetto Sequencer
description: Come creare la directory radice del pacchetto Sequencer
author: dansimp
ms.assetid: 23fe28f1-c284-43ee-b8b7-1dfbed94eea5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5150e87915202794624b6c51510e56454d2c7d36
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817616"
---
# Come creare la directory radice del pacchetto Sequencer


La directory radice del pacchetto è la directory nel computer che esegue App-V Sequencer in cui sono installati i file per l'applicazione sequenziata. Questa directory esiste anche virtualmente nel computer in cui verrà trasmessa un'applicazione sequenziata. Devi creare la directory radice del pacchetto prima di monitorare l'installazione di una nuova applicazione.

Dopo aver creato la directory radice del pacchetto, è possibile iniziare a sequenziare le applicazioni. Per altre informazioni sulla sequenziazione di una nuova applicazione, vedere [come sequenziare un'applicazione](how-to-sequence-an-application.md).

**Per creare la directory radice del pacchetto**

1.  Per creare la directory radice del pacchetto, nel computer in cui è in uso l'App-V Sequencer eseguire il mapping dell'unità Q:\\ al percorso di rete specificato. La posizione specificata dovrebbe avere spazio sufficiente per salvare l'applicazione che si sta sequenziando.

2.  Per creare una directory che è possibile usare per una nuova applicazione virtuale, creare una cartella nell'unità Q:\\ e assegnarle un nome.

    **Importante**  Il nome assegnato ai file delle applicazioni virtuali che verranno salvati nella directory radice del pacchetto deve usare il formato di denominazione di 8,3. I nomi di file non devono avere più di 8 caratteri con un'estensione di file di tre caratteri.

     

## Argomenti correlati


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[Come modificare il percorso della directory di registro](how-to-modify-the-log-directory-location.md)

[Come modificare il percorso della directory dei file temporanei](how-to-modify-the-scratch-directory-location.md)

 

 





