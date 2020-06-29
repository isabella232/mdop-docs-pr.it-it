---
title: Codici di errore della riga di comando di Sequencer
description: Codici di errore della riga di comando di Sequencer
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815556"
---
# Codici di errore della riga di comando di Sequencer


Usare l'elenco seguente per identificare gli errori correlati alla sequenziazione delle applicazioni tramite la riga di comando. Queste informazioni possono essere visualizzate anche visualizzando il file di log sequencer di App-V associato.

**Nota**  Durante la sequenziazione si possono verificare più errori e, in questo caso, il codice di errore visualizzato potrebbe essere la somma di due codici di errore. Ad esempio, se mancano i parametri */InstallPath* e */outputfile* , l'App-V sequencer restituirà **96**, ovvero la somma dei due codici di errore.

 

<a href="" id="01"></a>01  
Si è verificato un errore non specificato.

<a href="" id="02"></a>02  
La directory di installazione specificata (/INSTALLPACKAGE) non è valida.

<a href="" id="04"></a>04  
La directory radice del pacchetto specificata (/INSTALLPATH) non è valida.

<a href="" id="08"></a>08  
Il parametro */outputfile* specificato non è valido.

<a href="" id="16"></a>16  
La directory di installazione (/INSTALLPACKAGE) non è specificata.

<a href="" id="32"></a>32  
La directory radice del pacchetto (/INSTALLPATH) non è specificata.

<a href="" id="64"></a>64  
Il parametro */outputfile* non è specificato.

<a href="" id="128"></a>128  
L'unità di virtualizzazione dell'applicazione specificata non è valida.

<a href="" id="256"></a>256  
Il programma di installazione non è riuscito.

<a href="" id="512"></a>512  
La sequenziazione dell'applicazione non è riuscita.

<a href="" id="1024"></a>1024  
La valutazione delle scelte rapide installate non è riuscita.

<a href="" id="2048"></a>2048  
Non è possibile salvare il pacchetto dell'applicazione sequenziata.

<a href="" id="4096"></a>4096  
Il nome del pacchetto specificato (/PACKAGENAME) non è valido.

<a href="" id="8192"></a>8192  
La dimensione del blocco specificata (/BLOCKSIZE) non è valida.

<a href="" id="16384"></a>16384  
Il tipo di compressione specificato (/COMPRESSION) non è valido.

<a href="" id="32768"></a>32768  
Il percorso del progetto specificato non è valido.

<a href="" id="65536"></a>65536  
Il parametro di aggiornamento specificato non è valido.

<a href="" id="131072"></a>131072  
Il parametro del progetto di aggiornamento specificato non è valido.

<a href="" id="262144"></a>262144  
Il parametro path Decode specificato non è valido.

<a href="" id="525288"></a>525288  
Il nome del pacchetto non è specificato.

## Argomenti correlati


[Riferimento per Application Virtualization Sequencer](application-virtualization-sequencer-reference.md)

[Parametri della riga di comando di Sequencer](sequencer-command-line-parameters.md)

 

 





