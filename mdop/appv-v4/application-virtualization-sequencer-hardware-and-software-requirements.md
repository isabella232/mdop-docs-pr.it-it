---
title: Requisiti hardware e software per Application Virtualization Sequencer
description: Requisiti hardware e software per Application Virtualization Sequencer
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819625"
---
# Requisiti hardware e software per Application Virtualization Sequencer


Questo argomento descrive i requisiti hardware e software minimi consigliati per il computer che gestisce Microsoft Application Virtualization (App-V) Sequencer.

**Importante**  Devi eseguire l'App-V Sequencer (**SFTSequencer.exe**) usando un account con privilegi di amministratore a causa delle modifiche apportate dal sequencer al sistema locale. Queste modifiche possono includere la scrittura di file nella directory **C:\\Programmi files** , le modifiche del registro di sistema, l'avvio e l'arresto dei servizi, l'aggiornamento dei descrittori di sicurezza per i file e la modifica delle autorizzazioni.

 

Prima di installare il sequencer e dopo aver sequenziato ogni applicazione, è necessario ripristinare un'immagine del sistema operativo pulito nel computer di sequenziazione. Puoi usare uno dei metodi seguenti per ripristinare il computer che sta eseguendo il sequencer:

-   Riformattare il disco rigido e reinstallare il sistema operativo.

-   Ripristinare il disco rigido nel computer in cui è in uso l'immagine del sequencer usando un altro software per la creazione di immagini disco.

-   Ripristinare un'immagine del sistema operativo virtuale, ad esempio un'immagine di Microsoft Virtual PC. L'uso di una macchina virtuale consente di riutilizzare facilmente gli ambienti di sequenziazione con l'amministrazione minima.

L'elenco seguente descrive i requisiti hardware consigliati per l'uso dell'App-V Sequencer.

I requisiti sono elencati per primo per Microsoft Application Virtualization (App-V) 4.6 SP2, seguiti dai requisiti per le versioni che hanno preceduto l'App-V 4.6 SP2.

### <a href="" id="hardware-requirements-"></a>Requisiti hardware

-   Processore: Intel Pentium III, 1 GHz (32 bit o 64 bit). Il processo di sequenziazione è un processo a thread singolo e non sfrutta i processori duali.

-   Memoria-1GB o superiore, 2GB consigliata.

-   Disco rigido: spazio su disco rigido da 40 gigabyte (GB) con un minimo di 15 GB di spazio disponibile su disco rigido. Ti consigliamo di avere almeno tre volte lo spazio sul disco rigido necessario per l'applicazione in sequenza.

    **Nota**  La sequenziazione richiede l'utilizzo di dischi pesanti. Una velocità del disco veloce può diminuire il tempo di sequenziazione.

     

### Requisiti software per App-V 4,6 SP2

L'elenco seguente descrive i sistemi operativi supportati per l'uso dell'App-V 4,6 SP2 Sequencer.

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
<td align="left"><p>SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise o Ultimate</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professionale, aziendale o finale</p></td>
<td align="left"><p>Nessun Service Pack o SP1</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Pro o Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
</tbody>
</table>

 

**Nota**  Il sequencer di Application Virtualization (App-V) 4,6 SP2 supporta versioni a 32 bit e 64 bit di questi sistemi operativi.

 

È consigliabile configurare i computer che eseguono il sequencer con le stesse applicazioni installate nei computer di destinazione.

### Requisiti software per le versioni che precedono l'App-V 4,6 SP2

L'elenco seguente descrive i sistemi operativi supportati per l'uso del sequencer per le versioni precedenti a App-V 4,6 SP2.

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

### Requisiti software per Servizi Desktop remoti per App-V 4,6 SP2

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
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
</tbody>
</table>

 

**Nota**  Application Virtualization (App-V) 4,6 SP2 per Servizi Desktop remoto supporta versioni a 32 bit e a 64 bit di questi sistemi operativi.

 

### Requisiti software per i Servizi Desktop remoto per le versioni che precedono l'App-V 4,6 SP2

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
<td align="left"><p>Nessun Service Pack o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

**Nota**  Application Virtualization (App-V) 4,6 SP2 per Servizi Desktop remoto supporta versioni a 32 bit e a 64 bit di questi sistemi operativi.

 

## Argomenti correlati


[Requisiti hardware e software per Application Virtualization Client](application-virtualization-client-hardware-and-software-requirements.md)

[Requisiti di sistema di Application Virtualization](application-virtualization-system-requirements.md)

[Come installare Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)

[Come eseguire l'aggiornamento di Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





