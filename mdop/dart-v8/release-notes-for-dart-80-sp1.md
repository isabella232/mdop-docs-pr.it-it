---
title: Note sulla versione per DaRT 8.0 SP1
description: Note sulla versione per DaRT 8.0 SP1
author: dansimp
ms.assetid: fa7512d8-fb00-4c27-8f65-c15f3a8ff1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a4c49d12fed07f507d2db4d56969d8e7b0559c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824775"
---
# Note sulla versione per DaRT 8.0 SP1


**Per cercare queste note sulla versione, premere CTRL + F.**

Leggere accuratamente queste note sulla versione prima di installare Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 Service Pack 1 (SP1).

Queste note sulla versione contengono informazioni necessarie per installare correttamente la diagnostica e il set di strumenti di ripristino 8,0 SP1. Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altra documentazione DaRT, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Informazioni sulla documentazione del prodotto


Per informazioni sulla documentazione per DaRT, vedere la [Home page di Dart](https://go.microsoft.com/fwlink/?LinkID=252096) in Microsoft TechNet.

## Problemi noti di DaRT 8,0 SP1


### Ripristino configurazione di sistema non riesce quando si esegue un fabbro o un editor del registro

Se si esegue fabbro, editor del registro di sistema e, eventualmente, altri strumenti, ripristino configurazione di rete non riesce.

**Soluzione alternativa:** Chiudere e riavviare il dardo e quindi avviare Ripristino configurazione di sistema.

### L'analisi SFC non viene eseguita dopo l'avvio e la chiusura di fabbro o Gestione computer

Se si avvia e quindi si chiudono gli strumenti di gestione del fabbro o del computer, non è possibile eseguire Verifica file di sistema.

**Soluzione alternativa:** Chiudere e riavviare il dardo e quindi avviare SFC.

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> Il programma di installazione di DaRT non ha esito negativo quando ADK non è stato installato

Se si installa DaRT 8,0 SP1 usando la riga di comando per eseguire il file MSI e il ADK non è stato installato, l'installazione di DaRT dovrebbe avere esito negativo. Attualmente, il programma di installazione di DaRT 8,0 SP1 installa tutti i componenti tranne l'immagine di ripristino DaRT.

**Soluzione alternativa:** Nessuno.

### Il difensore non può essere lanciato dopo il lancio di fabbro, RegEdit, Crash Analyzer e gestione computer

Il difensore non viene avviato se sono già stati avviati fabbro, RegEdit, Crash Analyzer e gestione computer.

**Soluzione alternativa:** Chiudere e riavviare il dardo e quindi avviare Defender.

### Il difensore potrebbe essere lento all'avvio

Il difensore a volte richiede alcuni minuti per l'avvio. La barra di stato indica lo stato di caricamento corrente.

**Soluzione alternativa:** Nessuno.

## Informazioni sul copyright delle note sulla versione


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell sono marchi di fabbrica del gruppo Microsoft di società. Tutti gli altri marchi sono proprietà dei rispettivi proprietari.



## Argomenti correlati


[Informazioni su DaRT 8.0 SP1](about-dart-80-sp1.md)

 

 





