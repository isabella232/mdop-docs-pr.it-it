---
title: Come configurare il file di registro del client
description: Come configurare il file di registro del client
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817796"
---
# Come configurare il file di registro del client


Per configurare il file di log client Application Virtualization (App-V), è possibile usare le procedure seguenti.

**Per modificare il percorso del file di log**

-   Modificare il valore della chiave del registro di sistema seguente per specificare il nuovo percorso per il file di log. Dopo aver modificato questo valore, devi riavviare il servizio **sftlist** . Questa posizione può essere modificata anche in modo interattivo dopo l'installazione.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName

**Per modificare il livello di report del log**

-   Per impostazione predefinita, il tipo di messaggi scritti nel log include tutti gli eventi di livello di gravità 4 (informativo) o versioni successive. Il livello di gravità viene archiviato nel valore di chiave seguente. Impostare questo valore di chiave su 5 per abilitare la registrazione dettagliata. Usare la registrazione dettagliata solo per brevi periodi durante la risoluzione dei problemi perché genererà un volume molto elevato di messaggi e causerà il riempimento rapido del log.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity

**Per modificare le dimensioni del log**

-   In Application Virtualization (App-V) 4,5 la dimensione del log è controllata dal valore della chiave del registro di sistema seguente. Questo valore viene impostato su 256 MB e definisce le dimensioni massime, in MB, in cui il log può essere incrementato prima di essere reimpostato.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize

    **Attenzione**  Il valore della chiave del registro di sistema deve essere impostato su un valore maggiore di zero per verificare che il file di log venga reimpostato.

     

**Per modificare il numero di copie di backup**

-   Quando il file di log raggiunge la dimensione massima, viene forzata una reimpostazione quando si verifica la successiva scrittura nel log. Un reset causa la creazione di un nuovo file di log e il vecchio file viene rinominato come backup. L'impostazione seguente del registro di sistema controlla il numero di copie di backup del file di log che vengono mantenute quando il file viene reimpostato. Il valore predefinito è 4.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount

    Il formato dei nomi di file di log di backup è: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** e si basa sul tempo di reimpostazione, in UTC (Universal Coordinated Time). La tabella seguente elenca i simboli usati per creare i nomi di file e le relative descrizioni.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Simbolo</th>
    <th align="left">Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>AAAA</p></td>
    <td align="left"><p>anno a quattro cifre</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>MM</p></td>
    <td align="left"><p>mese a due cifre (01-12)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>DD</p></td>
    <td align="left"><p>giorno 2 cifre del mese (01 – 31)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>HH</p></td>
    <td align="left"><p>ora (00-23)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>mm</p></td>
    <td align="left"><p>minuti (00-59)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>ss</p></td>
    <td align="left"><p>secondi (00-59)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>UUU</p></td>
    <td align="left"><p>millisecondi (000-999)</p></td>
    </tr>
    </tbody>
    </table>

     

## Argomenti correlati


[Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





