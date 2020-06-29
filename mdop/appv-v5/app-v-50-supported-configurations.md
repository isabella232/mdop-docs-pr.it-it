---
title: Configurazioni supportate di App-V 5.0
description: Configurazioni supportate di App-V 5.0
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805991"
---
# Configurazioni supportate di App-V 5.0


Questo argomento specifica i requisiti necessari per installare ed eseguire Microsoft Application Virtualization (App-V) 5,0 nell'ambiente in uso.

**Importante**  
**Le configurazioni supportate in questo articolo si applicano solo a App-V 5,0**. Per le configurazioni supportate che si applicano ai Service Pack App-V 5,0, vedere le pagine Web seguenti:

-   [Novità in App-V 5.0 SP1](whats-new-in-app-v-50-sp1.md)

-   [Informazioni su App-V 5.0 SP2](about-app-v-50-sp2.md)

-   [Configurazioni supportate da App-V 5.0 SP3](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> Requisiti di sistema server App-V 5,0


**Importante**  
Il server App-V 5,0 non supporta gli scenari seguenti:



-   Distribuzione in un computer che esegue Microsoft Windows Server Core.

-   Distribuzione in un computer in cui è in esecuzione una versione precedente di componenti server App-V 5,0.

    **Nota**  
    È possibile installare l'App-V 5,0 affiancata con il solo server App-V 4,5 Lightweight streaming server (garanzia). La distribuzione di App-V 5,0 affiancata al server HWS (Application Virtualization Management Service) App-V 4,5 non è supportata.



-   Distribuzione in un computer che esegue Microsoft SQL Server Express Edition.

-   Distribuzione remota del database del server di gestione o del database di report. Il programma di installazione deve essere eseguito direttamente nel computer in cui è in esecuzione Microsoft SQL per l'installazione del database per avere esito positivo.

-   Distribuzione a un controller di dominio.

-   I percorsi brevi non sono supportati. Se si prevede di usare un breve percorso, è necessario creare un nuovo volume.

### Requisiti del sistema operativo del server di gestione

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di gestione App-V 5,0.

**Nota**  
Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita. Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.



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
<td align="left"><p>Microsoft Windows Server 2008 (standard, Enterprise, Datacenter o server Web)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1 e versioni successive</p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>



**Importante**  
La distribuzione del ruolo del server di gestione in un computer con funzionalità RDS (Remote Desktop Sharing) non è supportata.



### <a href="" id="management-server-hardware-requirements-"></a>Requisiti hardware del server di gestione

-   Processore-1,4 GHz o più veloce, processore a 64 bit (x64)

-   RAM — 1 GB di RAM (64 bit)

-   Spazio su disco: 200 MB di spazio disponibile su disco rigido, senza includere la directory di contenuto.

### Requisiti del sistema operativo di Publishing Server

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di pubblicazione App-V 5,0.

**Nota**  
Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita. Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.



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
<td align="left"><p>Microsoft Windows Server 2008 (standard, Enterprise, Datacenter o server Web)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a>Requisiti hardware del server di pubblicazione

-   Processore: 1,4 GHz o più veloce. processore a 64 bit (x64)

-   RAM — 2 GB di RAM (64 bit)

-   Spazio su disco: 200 MB di spazio disponibile su disco rigido. non inclusa la directory di contenuto

### Requisiti del sistema operativo per Reporting Server

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di report App-V 5,0.

**Nota**  
Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita. Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.



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
<td align="left"><p>Microsoft Windows Server 2008 (standard, Enterprise, Datacenter o server Web)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a>Requisiti hardware del server di Reporting

-   Processore: 1,4 GHz o più veloce. processore a 64 bit (x64)

-   RAM — 2 GB di RAM (64 bit)

-   Spazio su disco: 200 MB di spazio disponibile su disco rigido

### <a href="" id="sql-server-database-requirements-"></a>Requisiti di database di SQL Server

Nella tabella seguente sono elencate le versioni di SQL Server supportate per l'installazione di database e server di App-V 5,0.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo di server App-V 5,0</th>
<th align="left">Versione di SQL Server</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gestione/creazione di report</p></td>
<td align="left"><p>Microsoft SQL Server 2008</p>
<p>(Standard, Enterprise, Datacenter o Developer Edition con la caratteristica seguente: <strong> Servizi motore di database </strong> .)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestione/creazione di report</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p>
<p>(Standard, Enterprise, Datacenter o Developer Edition con la caratteristica seguente: <strong> Servizi motore di database </strong> .)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestione/creazione di report</p></td>
<td align="left"><p>Microsoft SQL Server 2012</p>
<p>(Standard, Enterprise, Datacenter o Developer Edition con la caratteristica seguente: <strong> Servizi motore di database </strong> .)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> Requisiti di sistema client App-V 5,0


Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del client App-V 5,0.

**Nota**  
Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita. Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.



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
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Windows 8,1 è supportato solo da App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
</tbody>
</table>



Gli scenari di installazione client App-V seguenti non sono supportati, ad eccezione di quanto indicato:

-   Computer che eseguono Windows Server

-   Computer che eseguono App-V 4,6 SP1 o versioni precedenti

-   Il client Servizi Desktop remoto di App-V 5,0 è supportato solo per i server abilitati per RDS

### <a href="" id="client-hardware-requirements-"></a>Requisiti hardware client

Nell'elenco seguente viene visualizzata la configurazione hardware supportata per l'installazione del client App-V 5,0.

-   Processore-1,4 GHz o più veloce a 32 bit (x86) o a 64 bit (x64)

-   RAM — 1 GB (32 bit) o 2 GB (64 bit)

-   Disk-100 MB per l'installazione, senza includere lo spazio su disco usato dalle applicazioni virtualizzate.

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> Requisiti di sistema client desktop remoto App-V 5,0


Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del client desktop remoto App-V 5,0.

**Nota**  
Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita. Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.



Sistema operativo Edition Service Pack Microsoft Windows Server 2008

R2

SP1

Microsoft Windows Server 2012

**Importante**  
Windows Server 2012 R2 è supportato solo da App-V 5,0 SP2



Microsoft Windows Server 2012 (standard, Datacenter)

R2

64 bit



### <a href="" id="remote-desktop-client-hardware-requirements-"></a>Requisiti hardware client desktop remoto

Nell'elenco seguente viene visualizzata la configurazione hardware supportata per l'installazione del client App-V 5,0.

-   Processore-1,4 GHz o più veloce a 32 bit (x86) o a 64 bit (x64)

-   RAM — 1 GB (32 bit) o 2 GB (64 bit)

-   Disk-100 MB per l'installazione, senza includere lo spazio su disco usato dalle applicazioni virtualizzate.

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> Requisiti di sistema sequencer App-V 5,0


La tabella seguente elenca i sistemi operativi supportati per l'installazione di Sequencer in App-V 5,0.

**Nota**  
Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita. Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.



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
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bit e 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bit e 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Windows 8,1 è supportato solo da App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2008</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bit e 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bit e 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Windows Server 2012 R2 è supportato solo da App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Microsoft Windows Server 2012</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a>Versioni supportate di System Center Configuration Manager


È possibile usare Microsoft System Center 2012 Configuration Manager o System Center 2012 R2 Configuration Manager per gestire le applicazioni virtuali App-V, i report e altre funzioni. La tabella seguente elenca le versioni supportate di Configuration Manager per ogni versione applicabile di App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione di Configuration Manager supportata</th>
<th align="left">Versione App-V</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gestione configurazione di Microsoft System Center 2012</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>System Center 2012 R2 Configuration Manager</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
</tbody>
</table>



Per altre informazioni su come si integra Configuration Manager con App-V, vedere [pianificazione dell'integrazione di App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).






## Argomenti correlati


[Pianificazione della distribuzione di App-V](planning-to-deploy-app-v.md)

[Prerequisiti di App-V 5.0](app-v-50-prerequisites.md)









