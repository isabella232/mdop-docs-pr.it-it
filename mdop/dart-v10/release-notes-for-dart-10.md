---
title: Note sulla versione per DaRT 10
description: Note sulla versione per DaRT 10
author: dansimp
ms.assetid: eb996980-f9c4-42cb-bde9-6b3d4b82b58c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 12ae5865538155f3c9ecf8b5f23b0d9e23232833
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822955"
---
# Note sulla versione per DaRT 10


**Per cercare queste note sulla versione, premere CTRL + F.**

Leggere accuratamente queste note sulla versione prima di installare Microsoft Diagnostics and Recovery Toolset (DaRT) 10.

Queste note sulla versione contengono informazioni necessarie per installare correttamente la diagnostica e il set di strumenti di ripristino 10. Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altra documentazione DaRT, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Problemi noti di DaRT 10


### Disk Commander non è in grado di ripristinare un record di avvio master danneggiato in una partizione fisica in Windows 10

In Windows 10 il "ripristinare il record di avvio Master (MBR) o l'intestazione dell'opzione GPT (GUID Partition Table)" in Disk Commander non è in grado di ripristinare un record di avvio master danneggiato in una partizione fisica e quindi non è in grado di avviare il computer client.

**Soluzione alternativa:** Avviare **ripristino avvio**, fare clic su **risoluzione dei problemi**, fare clic su **Opzioni avanzate**e quindi su **Avvia ripristino**.

### Più istanze di cancellazione disco destinate alla stessa unità causano tutte le istanze eccetto l'ultima per segnalare un errore

Se si avviano più istanze di wipe del disco e quindi si prova a pulire la stessa unità usando due istanze separate di cancellazione del disco, tutte le istanze eccetto l'ultima segnalano un errore di cancellazione dell'unità.

**Soluzione alternativa:** Nessuno.

### La cancellazione del disco potrebbe non cancellare tutti i dati sulle unità a stato solido che hanno memoria flash

Se si usa la cancellazione disco per cancellare i dati in un'unità SSD (Solid-State Drive) con memoria flash, non è possibile cancellare tutti i dati. Questo problema si verifica perché il firmware SSD controlla la posizione fisica delle Scritture durante l'esecuzione del disco Wipe.

**Soluzione alternativa:** Nessuno.

### Ripristino configurazione di sistema non riesce quando si esegue la procedura guidata o l'editor del registro

Se si esegue la procedura guidata fabbro, l'editor del registro di sistema e, eventualmente, altri strumenti, ripristino configurazione non riesce.

**Soluzione alternativa:** Chiudere e riavviare il dardo, quindi avviare Ripristino configurazione di sistema.

### L'analisi del file di sistema (SFC) non viene eseguita dopo l'avvio e la chiusura guidata di fabbro o Gestione computer

Se si avvia e quindi si chiude la procedura guidata o gli strumenti di gestione dei computer, il controllo file di sistema non viene eseguito.

**Soluzione alternativa:** Chiudere e riavviare il dardo, quindi avviare Controllo file di sistema.

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> Il programma di installazione di DaRT non viene superato quando il kit di valutazione e distribuzione di Windows non è installato

Se si installa il dardo 10 usando la riga di comando per eseguire il programma di installazione di Windows (con estensione msi) e il kit di valutazione e distribuzione di Windows (WindowsADK) non è stato installato, l'installazione di DaRT dovrebbe avere esito negativo. Attualmente, il programma di installazione di DaRT 10 installa tutti i componenti tranne l'immagine di ripristino DaRT.

**Soluzione alternativa:** Nessuno.

## Argomenti correlati


[Informazioni su DaRT 10](about-dart-10.md)

 

 





