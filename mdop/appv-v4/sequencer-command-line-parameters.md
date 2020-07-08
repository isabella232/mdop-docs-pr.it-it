---
title: Parametri della riga di comando di Sequencer
description: Parametri della riga di comando di Sequencer
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815555"
---
# Parametri della riga di comando di Sequencer


Puoi usare i parametri di sequencer di Application Virtualization (App-V) seguenti per sequenziare un'applicazione e aggiornare un'applicazione virtuale esistente usando una riga di comando. Per altre informazioni sulla sequenziazione di un'applicazione tramite una riga di comando, vedere [come sequenziare una nuova applicazione usando la riga di comando](how-to-sequence-a-new-application-by-using-the-command-line.md).

## Parametri della riga di comando di Sequencer


<a href="" id="-help-or---"></a>**/HELP o/?**  
Visualizza informazioni sui parametri disponibili per l'uso di una riga di comando per sequenziare le applicazioni.

<a href="" id="-installpackage-or--i"></a>**/INSTALLPACKAGE o/I**  
Specifica il Windows Installer o un file batch che verrà usato per installare un'applicazione in modo che possa essere sequenziata.

<a href="" id="-installpath-or--p"></a>**/INSTALLPATH o/P**  
Specifica la directory radice del pacchetto per un'applicazione.

<a href="" id="-outputfile-or--o"></a>**/OUTPUTFILE o/O**  
Specifica il percorso e il nome file del file SPRJ che verrà generato.

<a href="" id="-fullload-or--f"></a>**/FULLLOAD o/F**  
Specifica se tutti i file saranno contenuti nel blocco di funzionalità principale. Se il parametro **/FULLLOAD** è specificato nella riga di comando, tutti i dati dell'applicazione associata vengono aggiunti al blocco di funzionalità principale. Se il parametro **/FULLLOAD** non è specificato nella riga di comando, nessuno dei dati dell'applicazione associata verrà aggiunto al blocco di funzionalità principale.

<a href="" id="-packagename-or--k"></a>**/PACKAGENAME o/K**  
Specifica il nome del pacchetto che verrà assegnato all'applicazione sequenziata.

<a href="" id="-blocksize"></a>**/BLOCKSIZE**  
Specifica la dimensione del blocco di file SFT che verrà usata per trasmettere il pacchetto ai computer client. È possibile selezionare uno dei valori seguenti:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

Quando si specifica la dimensione del blocco, è consigliabile prendere in considerazione le dimensioni del file SFT. Un file con dimensioni di blocco più piccole richiede più tempo per eseguire il flusso sulla rete, ma è meno intensivo della larghezza di banda. I file con dimensioni di blocco più grandi usano più larghezza di banda della rete.

<a href="" id="-compression"></a>**/COMPRESSION**  
Specifica il metodo per la compressione del file SFT che verrà trasmesso al client.

<a href="" id="-msi-or--m"></a>**/MSI o/M**  
Specifica se deve essere creato un Windows Installer per l'applicazione sequenziata.

<a href="" id="-default"></a>**/DEFAULT**  
Specifica il file SPRJ predefinito che verrà usato per la creazione di un pacchetto di applicazione virtuale. Questo file viene usato come modello. sprj quando l'applicazione viene sequenziata per la prima volta.

<a href="" id="-upgrade"></a>**/UPGRADE**  
Specifica il percorso e il nome file del file SPRJ che verrà aggiornato.

<a href="" id="-decodepath"></a>**/DECODEPATH**  
Specifica la directory nel computer di sequenziazione in cui sono installati i file associati al pacchetto dell'applicazione sequenziata. Quando si specifica la directory, usare uno dei formati seguenti:

-   /DECODEPATH: Q:

-   /DECODEPATH: D:.

-   /DECODEPATH: "D:."

-   /DECODEPATH: "d:"

## Argomenti correlati


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[Codici di errore della riga di comando di Sequencer](sequencer-command-line-error-codes.md)

 

 





