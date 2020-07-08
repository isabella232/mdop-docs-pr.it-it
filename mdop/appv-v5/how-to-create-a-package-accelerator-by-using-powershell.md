---
title: Come creare un acceleratore pacchetto con PowerShell
description: Come creare un acceleratore pacchetto con PowerShell
author: dansimp
ms.assetid: 8e527363-d961-4153-826a-446a4ad8d980
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4270db9a5f0603cff1f33e6244a5abb517572d97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805620"
---
# Come creare un acceleratore pacchetto con PowerShell


Gli acceleratori del pacchetto App-V 5,0 sequenziano automaticamente le applicazioni grandi e complesse. Inoltre, quando applichi un Acceleratore pacchetto App-V 5,0, non sempre devi installare manualmente un'applicazione per creare il pacchetto virtualizzato.

**Per creare un Acceleratore pacchetto**

1.  Installare l'App-V 5,0 sequencer. Per altre informazioni sull'installazione del sequencer [, vedere come installare il sequencer](how-to-install-the-sequencer-beta-gb18030.md).

2.  Per aprire una console di PowerShell, fare clic su **Start** e digitare **PowerShell**. Fare clic con il pulsante destro del mouse su **Windows PowerShell** e scegliere **Esegui come amministratore**. Usa il cmdlet **New-AppvPackageAccelerator** .

3.  Per creare un Acceleratore pacchetto, assicurati di avere il pacchetto. AppV per creare un acceleratore, il supporto di installazione o i file di installazione e, facoltativamente, un file Leggimi per i consumatori dell'acceleratore da usare. I parametri seguenti sono necessari per usare il cmdlet Acceleratore pacchetto:

    -   **InstalledFilesPath** -specifica il percorso di installazione dell'applicazione.

    -   **Installer** : specifica il percorso del supporto del programma di installazione dell'applicazione

    -   **InputPackagePath** : specifica il percorso del pacchetto. AppV

    -   **Path** : specifica la directory di output per il pacchetto.

    L'esempio seguente mostra come creare un Acceleratore pacchetto con un pacchetto appv e il supporto di installazione:

    **New-AppvPackageAccelerator-InputPackagePath &lt; path to the. AppV file &gt; -percorso del programma di installazione &lt; per la directory del percorso eseguibile &gt; del programma di installazione &lt; del percorso di output&gt;**

    I parametri facoltativi aggiuntivi che possono essere usati con il cmdlet **New-AppvPackageAccelerator** vengono visualizzati nell'elenco seguente:

    -   **AcceleratorDescriptionFile** -specifica il percorso delle istruzioni per l'Acceleratore pacchetto creato dall'utente. Le istruzioni per l'acceleratore del pacchetto sono file di descrizione **txt** o **RTF** che verranno impacchettati con il pacchetto creato con l'Acceleratore pacchetto.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Amministrazione di App-V con PowerShell](administering-app-v-by-using-powershell.md)

 

 





