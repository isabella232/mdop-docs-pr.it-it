---
title: Come sequenziare un pacchetto usando PowerShell
description: Come sequenziare un pacchetto usando PowerShell
author: dansimp
ms.assetid: b41feed9-d1c5-48a3-940c-9a21d594f4f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbb9641ba75eda4d190892fa2bd0043c92ed9006
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805175"
---
# Come sequenziare un pacchetto usando PowerShell


Usare la procedura seguente per creare un nuovo pacchetto App-V 5,0 con PowerShell.

**Nota**  Prima di usare questa procedura, è necessario copiare i file del programma di installazione associati nel computer in cui è in corso il sequencer e leggere e comprendere la sezione sequencer della [pianificazione per l'App-V 5,0 sequencer e la distribuzione del client](planning-for-the-app-v-50-sequencer-and-client-deployment.md).

 

**Per creare una nuova applicazione virtuale tramite PowerShell**

1.  Installare l'App-V 5,0 sequencer. Per altre informazioni sull'installazione del sequencer [, vedere come installare il sequencer](how-to-install-the-sequencer-beta-gb18030.md).

2.  Per aprire una console di PowerShell, fare clic su **Start** e digitare **PowerShell**. Fare clic con il pulsante destro del mouse su **Windows PowerShell** e scegliere **Esegui come amministratore**.

3.  Usando la console di PowerShell, digitare quanto segue: **Import-Module appvsequencer**.

4.  Per creare un pacchetto, usa il cmdlet **New-AppvSequencerPackage** . Per creare un pacchetto sono necessari i parametri seguenti:

    -   **Nome** : specifica il nome del pacchetto.

    -   **PrimaryVirtualApplicationDirectory** -specifica il percorso della directory che verrà usata per installare l'applicazione. Questo percorso deve esistere.

    -   **Installer** : specifica il percorso del programma di installazione dell'applicazione associato.

    -   **Path** : specifica la directory di output per il pacchetto.

    Ad esempio:

    **New-AppvSequencerPackage-nome &lt; del pacchetto-percorso di PrimaryVirtualApplicationDirectory del percorso del &gt; &lt; pacchetto radice &gt; -programma &lt; di installazione per l'eseguibile del programma di installazione &gt; - &lt; directory OutputPath del percorso di output&gt;**

    Attendere che il sequencer crei il pacchetto. La creazione di un pacchetto tramite PowerShell può richiedere tempo. Se il pacchetto non è stato creato correttamente, verrà restituito un errore.

    L'elenco seguente mostra i parametri facoltativi aggiuntivi che possono essere usati con il cmdlet **New-AppvSequencerPackage** :

    -   AcceleratorFilePath: specifica il percorso del file Accelerator. cab per generare un pacchetto.

    -   InstalledFilesPath-specifica il percorso in cui vengono salvati i file locali installati dell'applicazione.

    -   InstallMediaPath-specifica il percorso in cui si trova il supporto di installazione

    -   TemplateFilePath: specifica il percorso di un file modello se si vuole personalizzare il processo di sequenziazione.

    -   FullLoad-specifica che il pacchetto deve essere completamente scaricato nel computer in cui è in uso l'App-V 5,0 prima che possa essere aperto.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Amministrazione di App-V con PowerShell](administering-app-v-by-using-powershell.md)

 

 





