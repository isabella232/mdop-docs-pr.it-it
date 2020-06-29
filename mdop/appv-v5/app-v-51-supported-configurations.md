---
title: Configurazioni supportate di App-V 5.1
description: Configurazioni supportate di App-V 5.1
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805943"
---
# Configurazioni supportate di App-V 5.1

>Si applica a: Windows 10, versione 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (aggiornamento della sicurezza esteso)

Questo argomento specifica i requisiti per installare ed eseguire Microsoft Application Virtualization (App-V) 5,1 nell'ambiente in uso.

## Requisiti di sistema di App-V Server

Questa sezione elenca i requisiti hardware e del sistema operativo per tutti i componenti di App-V Server.

### Scenari server App-V 5,1 non supportati

Il server App-V 5,1 non supporta gli scenari seguenti:

-   Distribuzione in un computer che esegue Microsoft Windows Server Core.

-   Distribuzione in un computer in cui è in esecuzione una versione precedente di componenti server App-V 5,1. È possibile installare l'App-V 5,1 affiancata al solo server App-V 4.5 Lightweight streaming server (garanzia). La distribuzione di App-V affiancata al server HWS (Application Virtualization Management Service) App-V 4,5 non è supportata.

-   Distribuzione in un computer che esegue Microsoft SQL Server Express Edition.

-   Distribuzione a un controller di dominio.

-   Percorsi brevi. Se si prevede di usare un breve percorso, è necessario creare un nuovo volume.

### Requisiti del sistema operativo del server di gestione

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di gestione App-V 5,1.

> [!NOTE]
> Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita. Per altre informazioni, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976) di supporto del ciclo di vita del supporto Microsoft

 | Sistema operativo                 | Service Pack | Architettura di sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bit       |
| Microsoft Windows Server 2016    |              |        64 bit       |
| Microsoft Windows Server 2012 R2 |              |        64 bit       |
| Microsoft Windows Server 2012    |              |        64 bit       |
| [Aggiornamento della sicurezza estesa](https://www.microsoft.com/windows-server/extended-security-updates) di Microsoft Windows Server 2008 R2|      SP1     |        64 bit       |
 

**Importante**  La distribuzione del ruolo del server di gestione in un computer con funzionalità RDS (Remote Desktop Sharing) non è supportata.

 

### <a href="" id="management-server-hardware-requirements-"></a>Requisiti hardware del server di gestione

-   Processore-1,4 GHz o più veloce, processore a 64 bit (x64)

-   RAM — 1 GB di RAM (64 bit)

-   Spazio su disco: 200 MB di spazio disponibile su disco rigido, senza includere la directory di contenuto

### Requisiti per il database del server di gestione

Nella tabella seguente sono elencate le versioni di SQL Server supportate per l'installazione di database di gestione di App-V 5,1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione di SQL Server</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2019</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
</tbody>
</table>

Per altre informazioni sui file di configurazione degli utenti con SQL Server 2016 o versione successiva, vedere l' [articolo del supporto](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).

### Requisiti del sistema operativo di Publishing Server

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di pubblicazione App-V 5,1.

| Sistema operativo                 | Service Pack | Architettura di sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bit       |
| Microsoft Windows Server 2016    |              |        64 bit       |
| Microsoft Windows Server 2012 R2 |              |        64 bit       |
| Microsoft Windows Server 2012    |              |        64 bit       |
| [Aggiornamento della sicurezza estesa](https://www.microsoft.com/windows-server/extended-security-updates) di Microsoft Windows Server 2008 R2 |      SP1     |        64 bit       |

### <a href="" id="publishing-server-hardware-requirements-"></a>Requisiti hardware del server di pubblicazione

App-V non aggiunge requisiti aggiuntivi oltre a quelli di Windows Server.

-   Processore-1,4 GHz o più veloce, processore a 64 bit (x64)

-   RAM — 2 GB di RAM (64 bit)

-   Spazio su disco: 200 MB di spazio disponibile su disco rigido, senza includere la directory di contenuto

### Requisiti del sistema operativo per Reporting Server

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di report App-V 5,1.

| Sistema operativo                 | Service Pack | Architettura di sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bit       |
| Microsoft Windows Server 2016    |              |        64 bit       |
| Microsoft Windows Server 2012 R2 |              |        64 bit       |
| Microsoft Windows Server 2012    |              |        64 bit       |
| [Aggiornamento della sicurezza estesa](https://www.microsoft.com/windows-server/extended-security-updates) di Microsoft Windows Server 2008 R2 |      SP1     |        64 bit       |

### <a href="" id="reporting-server-hardware-requirements-"></a>Requisiti hardware del server di Reporting

App-V non aggiunge requisiti aggiuntivi oltre a quelli di Windows Server.

-   Processore-1,4 GHz o più veloce, processore a 64 bit (x64)

-   RAM — 2 GB di RAM (64 bit)

-   Spazio su disco: 200 MB di spazio disponibile su disco rigido

### Requisiti del database del server di report

Nella tabella seguente sono elencate le versioni di SQL Server supportate per l'installazione del database di report App-V 5,1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione di SQL Server</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a>Requisiti di sistema client App-V

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del client App-V 5,1.

> [!NOTE]
> Con il rilascio di Windows 10 Anniversary (aka versione 1607), il client App-V è in-box e blocca l'installazione di qualsiasi versione precedente del client App-V

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows10 (versione precedente a 1607)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
</tbody>
</table>

 

Gli scenari di installazione client App-V seguenti non sono supportati, ad eccezione di quanto indicato:

-   Computer che eseguono Windows Server

-   Computer che eseguono App-V 4.6 SP1 o versioni precedenti

-   Il client Servizi Desktop remoto di App-V 5,1 è supportato solo per i server abilitati per RDS

### <a href="" id="app-v-client-hardware-requirements-"></a>Requisiti hardware client App-V

Nell'elenco seguente viene visualizzata la configurazione hardware supportata per l'installazione del client App-V 5,1.

-   Processore-1,4 GHz o più veloce a 32 bit (x86) o a 64 bit (x64)

-   RAM — 1 GB (32 bit) o 2 GB (64 bit)

-   Disk-100 MB per l'installazione, senza includere lo spazio su disco usato dalle applicazioni virtualizzate.

## Requisiti di sistema client di Servizi Desktop remoto


Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione client RDS (Remote Desktop Services) di App-V 5,1.

| Sistema operativo                 | Service Pack | Architettura di sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bit       |
| Microsoft Windows Server 2016    |              |        64 bit       |
| Microsoft Windows Server 2012 R2 |              |        64 bit       |
| Microsoft Windows Server 2012    |              |        64 bit       |
| [Aggiornamento della sicurezza estesa](https://www.microsoft.com/windows-server/extended-security-updates) di Microsoft Windows Server 2008 R2 |      SP1     |        64 bit       |

### Requisiti hardware client di Servizi Desktop remoto

App-V non aggiunge requisiti aggiuntivi oltre a quelli di Windows Server.

-   Processore-1,4 GHz o più veloce, processore a 64 bit (x64)

-   RAM — 2 GB di RAM (64 bit)

-   Spazio su disco: 200 MB di spazio disponibile su disco rigido

## Requisiti di sistema sequencer

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione di sequencer App-V 5,1.

| Sistema operativo                 | Service Pack | Architettura di sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bit       |
| Microsoft Windows Server 2016    |              |        64 bit       |
| Microsoft Windows Server 2012 R2 |              |        64 bit       |
| Microsoft Windows Server 2012    |              |        64 bit       |
| [Aggiornamento della sicurezza estesa](https://www.microsoft.com/windows-server/extended-security-updates) di Microsoft Windows Server 2008 R2 |      SP1     |        64 bit       |
| Microsoft Windows 10             |              | 32 bit e 64 bit   |
| Microsoft Windows 8,1            |              | 32 bit e 64 bit   |
| Microsoft Windows 7              |      SP1     | 32 bit e 64 bit   |

### Requisiti hardware sequencer

Vedere la documentazione di Windows o Windows Server per i requisiti hardware. App-V non aggiunge requisiti hardware aggiuntivi.

## <a href="" id="bkmk-supp-ver-sccm"></a>Versioni supportate di System Center Configuration Manager

Il client App-V supporta le versioni seguenti di System Center Configuration Manager:

-   ConfigurationManager di MicrosoftSystemCenter2012

-   System Center 2012 R2 Configuration Manager

-   System Center 2012 R2 Configuration Manager SP1

La matrice di versioni di App-V e System Center Configuration Manager seguente mostra tutte le combinazioni supportate ufficialmente da App-V e Configuration Manager.

> [!NOTE]
> Sia App-V 4,5 che 4,6 hanno terminato il supporto mainstream.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione App-V</th>
<th align="left">System Center Configuration Manager 2007</th>
<th align="left">System Center 2012 Configuration Manager</th>
<th align="left">System Center Configuration Manager 2012 SP1</th>
<th align="left">System Center 2012 R2 Configuration Manager</th>
<th align="left">System Center 2012 R2 Configuration Manager SP1</th>
<th align="left">System Center Configuration Manager 2012 SP2</th>
<th align="left">System Center Configuration Manager versione 1511</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p>MSI-solo wrapper</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5.1</p></td>
<td align="left"><p>MSI-solo wrapper</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
</tbody>
</table>

 

Per altre informazioni su come si integra Configuration Manager con App-V, vedere [pianificazione dell'integrazione di App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).

## Argomenti correlati

[Pianificazione della distribuzione di App-V](planning-to-deploy-app-v51.md)

[Prerequisiti di App-V 5.1](app-v-51-prerequisites.md)
