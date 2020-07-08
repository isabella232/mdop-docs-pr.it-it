---
title: Scelta della versione di Gestione avanzata Criteri di gruppo da installare
description: Scelta della versione di Gestione avanzata Criteri di gruppo da installare
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: b09ea8161b6801c62552f1c0d0ef8455dc111e2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819096"
---
# Scelta della versione di Gestione avanzata Criteri di gruppo da installare


Ogni versione di MicrosoftAdvanced (Advanced Group Policy Management) supporta versioni specifiche del sistema operativo Windows. Ti consigliamo vivamente di eseguire il client Advanced Group Policy Management e il server Advanced Group Policy Management nella stessa linea di sistemi operativi. Ad esempio, Windows 10 con Windows Server 2016, Windows 8.1 con Windows Server2012 R2 e così via.

È consigliabile installare il server Advanced Group Policy Management nella versione più recente del sistema operativo nel dominio. Advanced Group Policy Management (GPMC) usa la console Gestione criteri di gruppo per eseguire il backup e il ripristino degli oggetti Criteri di gruppo. Poiché le versioni più recenti di GPMC includono altre impostazioni dei criteri che non sono disponibili nelle versioni precedenti, è possibile gestire altre impostazioni dei criteri usando la versione più recente del sistema operativo.

Tutte le versioni di Advanced Group Policy Management sono in grado di gestire solo le impostazioni dei criteri introdotte nella stessa versione o in una versione precedente del sistema operativo in cui è in esecuzione Advanced Group Policy Management. Ad esempio, se si installa Advanced Group Policy Management 4.0 SP2 in Windows Server 2012, è possibile gestire le impostazioni dei criteri introdotte in Windows Server 2012 o versioni precedenti, ma non è possibile gestire le impostazioni dei criteri introdotte in un secondo momento, in Windows 8.1 o Windows Server2012 R2.

Se la versione di GPMC nel server Advanced Group Policy Management è precedente alla versione nei computer usati dagli amministratori per gestire i criteri di gruppo, il server Advanced Group Policy Management non sarà in grado di archiviare le impostazioni dei criteri non disponibili nella versione precedente di GPMC. Per il foglio di calcolo delle impostazioni di Criteri di gruppo incluso in Windows, vedi [Informazioni di riferimento per le impostazioni di Criteri di gruppo per Windows e Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).

## ADVANCED GROUP POLICY MANAGEMENT 4.0 SP3


Se si usano computer che eseguono Windows 10 per gestire i GPO, è necessario usare Advanced Group Policy Management 4,0 SP3. Non è possibile installare versioni precedenti di Advanced Group Policy Management nei computer che eseguono il sistema operativo Windows 10.

La tabella 1 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4.0 SP3 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0 SP3.

**Tabella 1: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4,0 SP3**

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
<td align="left"><p>Windows Server 2016 o Windows 10</p></td>
<td align="left"><p>Windows Server 2016 o Windows 10</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2</p></td>
<td align="left"><p>Windows10</p></td>
<td align="left"><p>Supportato con i caveat delineati in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> KB 4015786</a>
</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 o Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 o Windows 8,1</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o WindowsVista con Service Pack 1 (SP1)</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</p></td>
<td align="left"><p>Non supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</p></td>
</tr>
</tbody>
</table>

 

## ADVANCED GROUP POLICY MANAGEMENT 4.0 SP2


Se si usano computer che eseguono Windows Server2012 R2 o Windows 8.1 per gestire i GPO, è necessario usare Advanced Group Policy Management 4.0 SP2. Non è possibile installare versioni precedenti di Advanced Group Policy Management nei computer che eseguono tali sistemi operativi.

La tabella 1 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4.0 SP2 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0 SP2.

**Tabella 2: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0 SP2**

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
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 o Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 o Windows 8,1</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o WindowsVista con Service Pack 1 (SP1)</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Non supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</p></td>
</tr>
</tbody>
</table>

 

## ADVANCED GROUP POLICY MANAGEMENT 4.0 SP1


La tabella 2 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4,0 SP1 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0 SP1.

**Tabella 3: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0 SP1**

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
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8,1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</p></td>
</tr>
</tbody>
</table>

 

## Advanced Group Policy Management 4.0


La tabella 3 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4,0 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0.

**Tabella 4: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistemi operativi supportati per il server Advanced Group Policy Management</th>
<th align="left">Sistemi operativi supportati per il client Advanced Group Policy Management</th>
<th align="left">Supporto per Advanced Group Policy</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Non supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</p></td>
</tr>
</tbody>
</table>

 

## Versioni di Advanced Group Policy Management che precedono Advanced Group Policy Management 4.0


La tabella 4 elenca i sistemi operativi in cui è possibile installare le versioni di Advanced Group Policy Management che precedono Advanced Group Policy Management 4.0. Se un sistema operativo non è elencato, non è possibile installare Advanced Group Policy Management in tale sistema operativo.

**Tabella 5: sistemi operativi supportati per le versioni di Advanced Group Policy Management che precedono Advanced Group Policy Management 4.0**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Versione di Advanced Group Policy Management che può essere installata</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>3,0</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista con SP1</p></td>
<td align="left"><p>3,0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WindowsVista con nessun Service Pack installato (32 bit)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 (32 bit)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
</tbody>
</table>

 

## Come ottenere le tecnologie MDOP


Advanced Group Policy Management 4,0 SP2 fa parte di Microsoft Desktop Optimization Pack (MDOP). MDOP fa parte di Microsoft Software Assurance. Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Argomenti correlati


[Gestione avanzata Criteri di gruppo](index.md)

 

 





