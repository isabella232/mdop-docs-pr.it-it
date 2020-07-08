---
title: Configurazione delle funzionalità server di MBAM 2.5
description: Configurazione delle funzionalità server di MBAM 2.5
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823056"
---
# Configurazione delle funzionalità server di MBAM 2.5


Usare queste informazioni come punto di partenza per configurare le caratteristiche del server di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5 dopo l' [installazione del software mbam 2,5 Server](installing-the-mbam-25-server-software.md). Esistono due metodi che è possibile usare per configurare MBAM:

-   Configurazione guidata server MBAM

-   Cmdlet di Windows PowerShell

## Prima di iniziare a configurare le caratteristiche del server MBAM


Esaminare e completare i passaggi seguenti prima di iniziare a configurare le caratteristiche del server MBAM:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Dove ottenere le istruzioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Esaminare l'architettura consigliata per MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Architettura di alto livello per MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Esaminare le configurazioni supportate per MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurazioni supportate di MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Completare i prerequisiti necessari per ogni server.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Installare il software MBAM server su ogni server in cui verrà configurata una caratteristica del server MBAM.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installazione del software per il server di MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Esaminare i prerequisiti per l'uso di Windows PowerShell per configurare le caratteristiche del server MBAM (se si usa questo metodo per configurare le caratteristiche del server MBAM).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>

 

## Procedura per la configurazione delle funzionalità di MBAM server


Ogni riga della tabella seguente descrive le caratteristiche che verranno configurate in un server distinto, in base all' [architettura di alto livello consigliata per MBAM 2,5](high-level-architecture-for-mbam-25.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Caratteristiche da installare</th>
<th align="left">Dove ottenere le istruzioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurare i database.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Come configurare i database di MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare i report.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Come configurare i report di MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurare le applicazioni Web.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Come configurare le applicazioni Web di MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare l'integrazione di System Center Configuration Manager (se applicabile).</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager</a></p></td>
</tr>
</tbody>
</table>

 

Per un elenco degli eventi relativi alla configurazione delle funzionalità di MBAM server, vedere [log eventi del server](server-event-logs.md).



## Argomenti correlati


Configurazione delle funzionalità server di MBAM 2.5
 

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




