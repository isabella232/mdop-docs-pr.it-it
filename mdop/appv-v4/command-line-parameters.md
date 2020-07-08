---
title: Parametri della riga di comando
description: Parametri della riga di comando
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819405"
---
# Parametri della riga di comando


Usare i parametri sequencer di Application Virtualization seguenti per sequenziare un'applicazione e aggiornare un pacchetto di applicazione sequenziata al prompt dei comandi. Nella directory Microsoft Application Virtualization Sequencer Immetti **SFTSequencer**, seguito dal parametro appropriato.

<a href="" id="-help-or---"></a>*/Help* o */?*  
Consente di visualizzare l'elenco dei parametri disponibili per la sequenza della riga di comando.

<a href="" id="-installpackage-or--i"></a>*/InstallPackage* o */i*  
Consente di specificare il programma di installazione o un file batch per cui l'applicazione deve essere sequenziata.

<a href="" id="-installpath-or--p"></a>*/InstallPath* o */p*  
Consente di specificare la directory radice del pacchetto.

<a href="" id="-outputfile-or--o"></a>*/Outputfile* o */o*  
Consente di specificare il percorso e il nome file del file SPRJ che verrà generato.

**Importante**  Il parametro */outputfile* non è disponibile quando si apre un pacchetto che non si vuole aggiornare.

 

<a href="" id="-fullload-or--f"></a>*/FULLLOAD* o */f*  
Consente di specificare se inserire tutto nel blocco di funzionalità principale.

<a href="" id="-packagename-or--k"></a>*/PackageName* o */K*  
Consente di specificare il nome del pacchetto dell'applicazione sequenziata.

<a href="" id="-blocksize"></a>*/BLOCKSIZE*  
Specifica la dimensione del blocco di file SFT che verrà usata per trasmettere il pacchetto ai computer client. È possibile selezionare uno dei valori seguenti:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

Quando si specifica la dimensione del blocco, è consigliabile prendere in considerazione le dimensioni del file SFT. Un file con dimensioni di blocco più piccole richiede più tempo per eseguire il flusso sulla rete, ma è meno intensivo della larghezza di banda. I file con dimensioni di blocco più grandi usano più larghezza di banda della rete.

<a href="" id="-compression"></a>*/COMPRESSION*  
Consente di specificare il metodo per la compressione del file SFT mentre viene trasmesso al client.

<a href="" id="-msi-or--m"></a>*/MSI* o */m*  
Consente di specificare la generazione di un pacchetto di Microsoft Windows Installer per l'applicazione sequenziata.

<a href="" id="-default"></a>*/DEFAULT*  
Specifica il file SPRJ predefinito che verrà usato per la creazione di un pacchetto di applicazione virtuale. Questo file viene usato come modello. sprj quando l'applicazione viene sequenziata per la prima volta.

<a href="" id="-upgrade"></a>*/UPGRADE*  
Specifica il percorso e il nome file del file SPRJ che verrà aggiornato.

<a href="" id="-decodepath"></a>*/DECODEPATH*  
Specifica la directory nel computer di sequenziazione in cui sono installati i file associati al pacchetto dell'applicazione sequenziata. Quando si specifica la directory, usare uno dei formati seguenti:

-   /DECODEPATH: Q:

-   /DECODEPATH: D:.

-   /DECODEPATH: "D:."

-   /DECODEPATH: "d:"

## Argomenti correlati


[Informazioni sull'utilizzo della riga di comando di Sequencer](about-using-the-sequencer-command-line.md)

[Come aprire un'applicazione sequenziata usando la riga di comando](how-to-open-a-sequenced-application-using-the-command-line.md)

[Come aggiornare un pacchetto usando il comando Apri pacchetto](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





