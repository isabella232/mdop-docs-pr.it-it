---
title: Requisiti hardware e software per Sequencer
description: Requisiti hardware e software per Sequencer
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815535"
---
# Requisiti hardware e software per Sequencer


Questo argomento descrive i requisiti hardware e software minimi consigliati per il computer che gestisce Microsoft Application Virtualization (App-V) Sequencer.

Prima di installare il sequencer e dopo aver sequenziato ogni applicazione, è necessario ripristinare un'immagine del sistema operativo pulito nel computer di sequenziazione. Puoi usare uno dei metodi seguenti per ripristinare il computer che sta eseguendo il sequencer:

-   Riformattare il disco rigido e reinstallare il sistema operativo.

-   Ripristinare il disco rigido nel computer in cui è in uso l'immagine del sequencer usando un altro software per la creazione di immagini disco.

L'elenco seguente descrive i requisiti hardware consigliati per l'uso dell'App-V Sequencer.

### <a href="" id="hardware-requirements-"></a>Requisiti hardware

-   Processore: Intel Pentium III, 1 GHz (32 bit o 64 bit). Il processo di sequenziazione è un processo a thread singolo e non sfrutta i processori duali.

-   Memoria-1GB o superiore, 2 GB consigliati.

-   Disco rigido: spazio su disco rigido da 40 gigabyte (GB) con un minimo di 15 GB di spazio disponibile su disco rigido. Ti consigliamo di avere almeno tre volte lo spazio sul disco rigido necessario per l'applicazione in sequenza.

    **Nota**  La sequenziazione richiede l'utilizzo di dischi pesanti. Una velocità del disco veloce può diminuire il tempo di sequenziazione.

     

### Requisiti software

L'elenco seguente descrive i sistemi operativi supportati per l'uso del sequencer.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional</p></td>
<td align="left"><p>SP2 o SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise o Ultimate</p></td>
<td align="left"><p>Nessun Service Pack, SP1 o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7 ¹</p></td>
<td align="left"><p>Professionale, aziendale o finale</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

¹ supportato per App-V 4,5 con SP1 o SP2 e solo App-V 4,6

**Nota**  L'Application Virtualization (App-V) 4,6 Sequencer supporta versioni a 32 bit e 64 bit di questi sistemi operativi.

 

È consigliabile configurare i computer che eseguono il sequencer con le stesse applicazioni installate nei computer di destinazione.

### Requisiti software per Servizi Desktop remoto

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, aziendale o Datacenter</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

**Nota**  Application Virtualization (App-V) 4,6 per Servizi Desktop remoto supporta versioni a 32 bit e a 64 bit di questi sistemi operativi.

 

## Argomenti correlati


[Panoramica di Application Virtualization Sequencer](application-virtualization-sequencer-overview.md)

 

 





