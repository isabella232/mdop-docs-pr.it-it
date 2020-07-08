---
title: Informazioni su DaRT 7.0
description: Informazioni su DaRT 7.0
author: dansimp
ms.assetid: 217ffafc-6d73-4b80-88d9-71870460d4ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cd647b2f596ce88ce38580f08422ff8f92b35c06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823275"
---
# Informazioni su DaRT 7.0


Microsoft Diagnostics and Recovery Toolset (DaRT) 7 ti aiuta a risolvere i problemi e a ripristinare i desktop basati su Windows. Sono inclusi i desktop che non possono essere avviati. DaRT è un potente set di strumenti che estendono l'ambiente di ripristino di Windows (WinRE). Usando DaRT, puoi analizzare un problema per determinare la causa, ad esempio controllando il log eventi o il registro di sistema del computer.

DaRT offre anche strumenti che ti aiutano a risolvere un problema non appena ne determini la causa. Ad esempio, puoi usare gli strumenti di DaRT per disabilitare un driver di dispositivo difettoso, rimuovere gli hotfix, ripristinare i file eliminati e analizzare il computer per il malware anche quando non puoi o non devi avviare il sistema operativo Windows installato.

Il dardo consente di recuperare rapidamente i computer in cui è in esecuzione una versione a 32 bit o a 64 bit di Windows 7, in genere in meno tempo rispetto alla riimmagine del computer.

## Informazioni sull'immagine di ripristino di DaRT 7


La funzionalità in DaRT consente di creare un'immagine di ripristino basata su WinRE combinata con un set di strumenti forniti da DaRT. L'immagine di recupero dardo sfrutta WinRE, da cui è possibile accedere alla finestra del **set di strumenti di diagnostica e ripristino** .

Usare la **creazione guidata immagine di ripristino di freccette** per creare l'immagine di ripristino DaRT. Per impostazione predefinita, la procedura guidata crea un file di immagine ISO (International Organization for Standardizzation) sul desktop denominato DaRT70. ISO, anche se è possibile specificare un percorso e un nome file diversi. La procedura guidata consente inoltre di masterizzare l'immagine in un CD o un DVD. Dopo aver completato la procedura guidata, è possibile salvare l'immagine di ripristino in un'unità flash USB o salvarla in un formato che può essere usato per creare una partizione remota o una partizione di ripristino.

Quando devi usare DaRT per l'avvio di un computer per utenti finali che non si avvia, puoi seguire le istruzioni su [come recuperare i computer locali usando l'immagine di ripristino DaRT](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).

Per informazioni dettagliate sugli strumenti in DaRT, Vedi [Panoramica degli strumenti di dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).

## <a href="" id="what-s-new-in-dart-7"></a>Novità di DaRT 7


DaRT7 continua a supportare tutti gli scenari inclusi nelle versioni precedenti e aggiunge una nuova funzionalità di connessione remota oltre a tre nuove opzioni di distribuzione.

### Creazione di immagini DaRT 7

La procedura guidata che si usa per creare immagini ISO DaRT è ora chiamata **immagine di recupero Dart** e ora supporta un'opzione per abilitare o disabilitare la nuova funzionalità di connessione remota. Connessione remota consente a un agente dell'helpdesk di eseguire gli strumenti DaRT da una posizione remota. Nelle versioni precedenti l'agente dell'helpdesk doveva essere fisicamente presente nel computer dell'utente finale per eseguire gli strumenti DaRT.

La procedura guidata consente inoltre di personalizzare il messaggio di benvenuto per la funzionalità di connessione remota (il messaggio viene visualizzato quando gli utenti finali eseguono lo strumento di connessione remota). Gli amministratori IT possono anche configurare il numero di porta da usare per la connessione remota.

Per altre informazioni sulla creazione **guidata immagine di ripristino delle freccette** o sulla connessione remota, vedere [creare l'immagine di ripristino di DaRT 7,0](creating-the-dart-70-recovery-image-dart-7.md).

### Distribuzione ISO di DaRT 7

Oltre alla masterizzazione su CD o DVD, DaRT7 aggiunge tre nuove opzioni quando si distribuisce la ISO che contiene l'immagine di ripristino delle freccette:

-   Distribuzione di unità flash USB

-   Distribuzione di partizioni remote

-   Distribuzione della partizione di ripristino

L'opzione di distribuzione dell'unità flash USB consente a una società di usare il dardo in computer in cui non sono disponibili unità CD o DVD. Le opzioni di recupero e partizione remota consentono agli utenti finali di accedere facilmente all'immagine DaRT e di abilitare la funzionalità di connessione remota.

Per altre informazioni su come distribuire le immagini di ripristino delle freccette, vedere [distribuzione dell'immagine di ripristino di dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).

## Argomenti correlati


[Attività iniziali di DaRT 7.0](getting-started-with-dart-70-new-ia.md)

[Note sulla versione per DaRT 7.0](release-notes-for-dart-70-new-ia.md)

 

 





