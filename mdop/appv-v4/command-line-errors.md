---
title: Errori della riga di comando
description: Errori della riga di comando
author: dansimp
ms.assetid: eea62568-4e90-4877-9cc7-e27ef5c05068
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab29a77dc15a8c7bd3590b918a7ca8c1ca6e8c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819406"
---
# Errori della riga di comando


Usare l'elenco di errori seguente per identificare i motivi per cui la sequenziazione della riga di comando non funziona correttamente. È anche possibile visualizzare questi errori visualizzando il file di log del sequencer.

**Nota**  Durante la sequenziazione potrebbe essere visualizzato più di un errore. Inoltre, il codice di errore visualizzato può essere la somma di due codici di errore. Ad esempio, se i parametri */InstallPath* e */outputfile* sono mancanti, Microsoft System Center Application Virtualization Sequencer restituirà 96, ovvero la somma dei due codici di errore.

 

<a href="" id="01"></a>01  
Si è verificato un errore non specificato.

<a href="" id="02"></a>02  
La directory di installazione specificata (/INSTALLPACKAGE) specificata non è valida.

<a href="" id="04"></a>04  
La directory radice del pacchetto specificata (/INSTALLPATH) non è valida.

<a href="" id="08"></a>08  
Il parametro */outputfile* specificato non è valido.

<a href="" id="16"></a>16  
La directory di installazione (/INSTALLPACKAGE) non è stata specificata.

<a href="" id="32"></a>32  
La directory radice del pacchetto (/INSTALLPATH) non è stata specificata.

<a href="" id="64"></a>64  
Il parametro */outputfile* non è stato specificato.

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
La dimensione del blocco specificata (/BLOCKSIZE <em> ) </em> non è valida.

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
Il nome del pacchetto non è stato specificato.

## Argomenti correlati


[Informazioni sull'utilizzo della riga di comando di Sequencer](about-using-the-sequencer-command-line.md)

[Parametri della riga di comando](command-line-parameters.md)

 

 





