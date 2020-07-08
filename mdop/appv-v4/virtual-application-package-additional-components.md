---
title: Componenti aggiuntivi del pacchetto applicazione virtuale
description: Componenti aggiuntivi del pacchetto applicazione virtuale
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815076"
---
# Componenti aggiuntivi del pacchetto applicazione virtuale


App-V Sequencer ha rilevato una directory che contiene file eseguibili a 64 bit e a 32 bit e/o dll (Dynamic-Link Library) che dipendono dallo stesso assembly affiancato. In genere, il Sequencer crea assembly side-by-side privati per tutti gli assembly pubblici usati dal pacchetto. Tuttavia, non è possibile creare versioni a 32 bit e a 64 bit degli assembly privati nella stessa directory.

Se il sequencer rileva un singolo conflitto, eseguirà le operazioni seguenti:

-   Rimuovere tutti gli assembly privati a 64 bit esistenti nell'intero pacchetto, indipendentemente dal fatto che la directory abbia un conflitto.

-   Creare solo versioni a 32 bit degli assembly side-by-side privati.

È consigliabile installare in modo nativo le versioni pubbliche di tutti gli assembly di 64 bit necessari nel computer che eseguono Sequencer e in tutti i computer client App-V.

Per individuare gli assembly pubblici esistenti necessari, aprire la directory in cui viene salvato il pacchetto e cercare nella cartella **VFS** . Ad esempio, se la radice del pacchetto è **Q:\\MyApp**, quando si sequenzia l'applicazione, cercare in **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** e individuare tutti gli assembly pubblici esistenti. Le versioni a 64 bit di questi file inizieranno sempre con il testo seguente all'inizio del nome del manifesto: **amd64...**. Il nome e la versione esatta dell'assembly possono essere trovati nel file manifesto associato.

Usare uno dei collegamenti seguenti per scaricare e installare la versione corretta dei prerequisiti necessari:

-   [Pacchetto ridistribuibile di Microsoft Visual C++ 2005 (x64)](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [Pacchetto ridistribuibile di Microsoft Visual C++ 2005 SP1 (x64)](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [Pacchetto ridistribuibile di Microsoft Visual C++ 2008 (x64)](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [Pacchetto ridistribuibile di Microsoft Visual C++ 2008 SP1 (x64)](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





