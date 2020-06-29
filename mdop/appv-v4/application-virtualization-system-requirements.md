---
title: Requisiti di sistema di Application Virtualization
description: Requisiti di sistema di Application Virtualization
author: dansimp
ms.assetid: a2798dd9-168e-45eb-8103-e12e128fae7c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c160a7532b521bb41570b419b22b9e7daaec2987
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819516"
---
# Requisiti di sistema di Application Virtualization


Questo argomento descrive i requisiti hardware e software minimi per Microsoft Application Virtualization (App-V) Management Server e streaming server.

## Server di gestione e streaming di Application Virtualization


L'elenco seguente include i requisiti minimi hardware e software consigliati per App-V Management Server e App-V Streaming Server.

### Requisiti hardware

-   Processore: Intel Pentium III, 1 GHz

-   RAM-512 MB

-   Spazio su disco: 200 MB di spazio disponibile su disco rigido, senza includere la directory di contenuto

### Requisiti software

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
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ si applica solo a App-V 4,5 SP1 e SP2.

## Archivio dati


L'elenco seguente include i requisiti hardware e software consigliati minimi per il computer usato quando si installa l'archivio dati in un server separato. L'archivio dati è obbligatorio solo per il server di gestione della virtualizzazione dell'applicazione.

### Requisiti hardware

-   Processore: Intel Pentium III, 850 MHz

-   RAM-512 MB

-   Spazio su disco: 200 MB di spazio disponibile su disco rigido

### Requisiti software

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
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ si applica solo a App-V 4,5 SP1 e SP2.

-   Database: Microsoft SQL Server2000 SP3a o SP4, SQL Server2005 SP1, SP2 o SP3 o SQL Server2008, nessun Service Pack o SP1 o SQL Server2008 R2 (32 bit o 64 bit)

-   Componenti di Microsoft Data Access-MDAC 2,7

-   Controller di dominio: Servizi di dominio Active Directory o PDC (Primary Domain Controller) basato su Windows NT 4.0 come autorità di autenticazione centralizzata

## Servizio Web di gestione


L'elenco seguente include i requisiti hardware e software consigliati minimi per il servizio Web Application Virtualization Management quando è installato in un computer separato.

### Requisiti hardware

-   Processore: Intel Pentium III, 800 MHz

-   RAM: 256 MB

-   Spazio su disco: 50 MB di spazio disponibile su disco rigido

### Requisiti software

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
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ si applica solo a App-V 4,5 SP1 e SP2.

-   Internet Information Services-Internet Information Services (IIS) 6,0 configurato con Microsoft ASP.NET, IIS 7

-   Microsoft .NET Framework 2.0

## Console di gestione


L'elenco seguente include i requisiti hardware e software consigliati minimi per la console di gestione di Application Virtualization quando è installato in un computer separato.

### Requisiti hardware

-   Processore: Intel Pentium III, 450 MHz

-   RAM: 256 MB

-   Spazio su disco: 200 MB di spazio disponibile su disco rigido

### Requisiti software

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
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP2 o SP3</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise o Ultimate Edition</p></td>
<td align="left"><p>Nessun Service Pack, SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professional, Enterprise o Ultimate Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ si applica solo a App-V 4,5 SP1 e SP2.

-   Microsoft Management Console: MMC 3.0 o versioni successive

-   Microsoft .NET Framework 2.0 SP2 (minimo)

    **Importante**  Il requisito minimo è .NET Framework 2,0 SP2 se è necessario installare App-V hotfix KB980850 o gli hotfix successivi di App-V nel computer in cui è in uso la console di gestione di App-V.

     

## Argomenti correlati


[Requisiti hardware e software per Application Virtualization Client](application-virtualization-client-hardware-and-software-requirements.md)

[Requisiti hardware e software per Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)

[Come configurare i server per la distribuzione basata su server](how-to-configure-servers-for-server-based-deployment.md)

[Come installare i server e i componenti del sistema](how-to-install-the-servers-and-system-components.md)

[Come aggiornare i server e i componenti del sistema](how-to-upgrade-the-servers-and-system-components.md)

 

 





