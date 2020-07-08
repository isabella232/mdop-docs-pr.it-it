---
title: Come distribuire il client di MBAM usando una riga di comando
description: Come distribuire il client di MBAM usando una riga di comando
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824486"
---
# Come distribuire il client di MBAM usando una riga di comando


È possibile usare una riga di comando per distribuire il software client di amministrazione e monitoraggio di Microsoft BitLocker (MBAM).

## Riga di comando per distribuire il software del client MBAM


Digitare il comando seguente al prompt dei comandi per accettare automaticamente il contratto di licenza con l'utente finale quando si distribuisce il software client MBAM.

**MBAMClientSetup.exe/acceptEula = Yes**

**Nota**  Le opzioni della riga di comando **/Ju** e **/JM** non sono supportate e non possono essere usate per installare il software client mbam.

 

Digitare il comando seguente al prompt dei comandi per estrarre e installare l'MSP:

**MBAMClientSetup.exe &lt; percorso di/Extract per estrarre MSI &gt; /AcceptEula = Yes**

Installare quindi il file MSI in modo invisibile all'utente eseguendo il comando seguente:

**msiexec/i &lt; path to Estratto MSI &gt; /qb ALLUSERS = 1 REBOOT = ReallySuppress**

**Nota**  A partire da MBAM 2,5 SP1, un file MSI separato non è più incluso nel prodotto MBAM. È tuttavia possibile estrarre l'MSI dal file eseguibile (con estensione exe) incluso nel prodotto, dopo aver accettato l'EULA.

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a>OPTIn \ _FOR \ _MICROSOFT \ _UPDATES = 1 opzione della riga di comando


Facoltativamente, è possibile specificare l'opzione della riga `OPTIN_FOR_MICROSOFT_UPDATES=1` di comando durante l'installazione del software client per installare automaticamente gli aggiornamenti Microsoft nei computer client. Se specifichi questa opzione, Microsoft Update avvia automaticamente la ricerca degli aggiornamenti disponibili dopo il completamento dell'installazione del software client.

Puoi usare questa opzione della riga di comando con uno dei metodi di installazione seguenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Installare il software del client MBAM usando</th>
<th align="left">Esempio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>MBAMClientSetup.exe</strong></p></td>
<td align="left"><p><strong>MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>msiexec/i MBAMClient.msi</strong></p></td>
<td align="left"><p><strong>msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
</tbody>
</table>

 


## Argomenti correlati


[Distribuzione del client di MBAM 2.5](deploying-the-mbam-25-client.md)

 

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




