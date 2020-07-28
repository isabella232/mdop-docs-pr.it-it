---
title: Novità di Gestione avanzata Criteri di gruppo 4.0 SP3
description: Novità di Gestione avanzata Criteri di gruppo 4.0 SP3
author: dansimp
ms.assetid: df495d55-9fbf-4f7e-a7af-3905f4f8790e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 44e7dc6c5de75ae3a5e5def638974bae20ad2a1e
ms.sourcegitcommit: 594b6e431af98562e0b806e224d2c5c7e07d2c77
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/27/2020
ms.locfileid: "10895766"
---
# Novità di Gestione avanzata Criteri di gruppo 4.0 SP3


Questo contenuto descrive i miglioramenti e le configurazioni supportate per il servizio Pack3 (Advanced Group Policy Management) 4.0 (SP3). Se c'è una differenza tra questo contenuto e altre documentazioni di Advanced Group Policy Management, considera questo contenuto autorevole e presupponga che sostituisca l'altra documentazione.

## <a href="" id="what-s-new"></a>Novità


Advanced Group Policy Management 4.0 SP3 supporta le caratteristiche e le funzionalità seguenti.

### Supporto per Windows10

Advanced Group Policy Management 4.0 SP3 aggiunge il supporto per i sistemi operativi Windows10 e Windows Server 2016.

### Supporto per PowerShell

Advanced Group Policy Management 4.0 SP3 aggiunge il supporto per i cmdlet di PowerShell. Per un elenco dei cmdlet disponibili in Advanced Group Policy Management 4.0 SP3, incluse le descrizioni e la sintassi, vedere [automazione di Microsoft Desktop Optimization Pack con Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).

### Feedback dei clienti e aggiornamento cumulativo

Advanced Group Policy Management 4,0 SP3 include un rollup di tutte le correzioni fino a Microsoft Advanced Group Policy Manager 4,0 SP2 e tutte le correzioni per i problemi rilevati da Advanced Management Packers 4,0 SP2.

### Possibilità di eseguire l'aggiornamento a Advanced Group Policy Management 4.0 SP3 senza immettere di nuovo i parametri di configurazione

È possibile aggiornare il client Advanced Group Policy Management o il server Advanced Group Policy Management a Advanced Group Policy Management 4.0 SP3 senza che venga chiesto di immettere di nuovo i parametri di configurazione, detti Smart Upgrade, solo da Advanced Group Policy Management 4.0 e versioni successive, come illustrato nella tabella seguente. Se si esegue l'aggiornamento a Advanced Group Policy Management 4.0 SP3 da altre versioni di Advanced Group Policy Management, come illustrato nella tabella, è necessario usare l'aggiornamento classico, che richiede di immettere di nuovo i parametri di configurazione. Poiché ogni versione di Advanced Group Policy Management è associata a un particolare sistema operativo, vedere [scelta della versione di Advanced Group Policy per l'installazione](https://go.microsoft.com/fwlink/?LinkId=254350) e verificare che il sistema operativo venga aggiornato in modo appropriato prima di aggiornare Advanced Group Policy Management.

**Aggiornamenti supportati per Advanced Group Policy Management SP3 4,0**

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Versione Advanced Group Policy Management da cui è possibile eseguire l'aggiornamento</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
<td align="left"><p><strong>4,0 SP2</strong></p></td>
<td align="left"><p><strong>4,0 SP3</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento classico</p></td>
<td align="left"><p>Aggiornamento classico</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3,0</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento classico</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento intelligente</p></td>
<td align="left"><p>Aggiornamento intelligente</p></td>
<td align="left"><p>Aggiornamento intelligente</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,0 SP1</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento intelligente</p></td>
<td align="left"><p>Aggiornamento intelligente</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0 SP2</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento intelligente</p></td>
</tr>
</tbody>
</table>

 

## Configurazioni supportate


Advanced Group Policy Management 4.0 SP3 supporta le configurazioni nella tabella seguente. Anche se Advanced Group Policy Management supporta configurazioni miste, ti consigliamo vivamente di eseguire il client Advanced Group Policy Management e il server Advanced Group Policy Management nella stessa linea di sistema operativo, ad esempio Windows10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2 e così via.

**Sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0 SP3**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Configurazioni supportate per il server Advanced Group Policy Management</strong></th>
<th align="left"><strong>Configurazioni supportate per il client Advanced Group Policy Management</strong></th>
<th align="left"><strong>Supporto per Advanced Group Policy</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2019 o Windows 10</p></td>
<td align="left"><p>Windows10</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2016 o Windows 10</p></td>
<td align="left"><p>Windows10</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 o Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o WindowsVista con Service Pack 1 (SP1)</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Non supportato</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</p></td>
</tr>
</tbody>
</table>

 

## Prerequisiti per l'installazione di Advanced Group Policy Management 4.0 SP3

La tabella seguente descrive il comportamento dei programmi di installazione del client e del server di Advanced Group Policy Management 4.0 SP3 quando mancano le funzionalità di .NET Framework 4.5.1, PowerShell 3,0 o GPMC negli strumenti di amministrazione del server remoto.

| Client Advanced Group Policy            |                                                                                                 |                                                                            | Server Advanced Group Policy Management                                                                     |                                                                                                 |                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Sistema operativo       | .NET Framework                                                                                  | PowerShell                                                                 | Strumenti di amministrazione remota del server                                              | .NET Framework                                                                                  | Strumenti di amministrazione remota del server                                              |
| Windows10             | Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione. | Se PowerShell 3,0 non è installato, il programma di installazione blocca l'istallazione. | Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni. | Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione. | Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni. |
| Windows 8.1            | Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione. | Se PowerShell 3,0 non è installato, il programma di installazione blocca l'istallazione. | Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni. | Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione. | Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni. |
| Windows Server 2012 R2 | Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione. | Se PowerShell 3,0 non è installato, il programma di installazione blocca l'istallazione. | Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.   | Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione. | Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.   |

 

## Come ottenere le tecnologie MDOP


Advanced Group Policy Management 4,0 SP3 fa parte del Microsoft Desktop Optimization Pack (MDOP) a partire da MDOP 2015. MDOP fa parte di Microsoft Software Assurance. Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Argomenti correlati


[Gestione avanzata Criteri di gruppo](index.md)

[Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP3](release-notes-for-microsoft-advanced-group-policy-management-40-sp3.md)

[Scelta della versione di Gestione avanzata Criteri di gruppo da installare](choosing-which-version-of-agpm-to-install.md)

 

 





