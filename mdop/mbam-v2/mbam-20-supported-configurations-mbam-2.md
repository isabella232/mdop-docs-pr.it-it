---
title: Configurazioni supportate di MBAM 2.0
description: Configurazioni supportate di MBAM 2.0
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823906"
---
# Configurazioni supportate di MBAM 2.0


In questo argomento vengono specificati i requisiti per l'installazione e l'esecuzione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 nell'ambiente tramite la topologia autonoma. Per le configurazioni supportate che si applicano alle versioni successive, vedere la documentazione relativa alla versione applicabile.

Se si prevede di installare MBAM 2,0 usando la topologia di Configuration Manager e si vuole rivedere un elenco dei requisiti di sistema, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

La configurazione consigliata per l'uso di MBAM in un ambiente di produzione è con due server, a seconda dei requisiti di scalabilità. Questa configurazione supporta fino a 200.000 client MBAM. Per un'immagine e le descrizioni dell'infrastruttura server di MBAM autonoma, vedere [architettura di alto livello per mbam 2,0](high-level-architecture-for-mbam-20-mbam-2.md).

**Nota**  Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita. Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.

 

## <a href="" id="---------mbam-server-system-requirements"></a> Requisiti di sistema di MBAM server


### Requisiti del sistema operativo del server

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di amministrazione e monitoraggio di Microsoft BitLocker.

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
<td align="left"><p>WindowsServer2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2012</p></td>
<td align="left"><p>Versione standard o Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>

 

**Nota**  Non è disponibile alcun supporto per l'installazione di servizi, report o database di MBAM in un computer controller di dominio.

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a>Requisiti per Server Processor, RAM e spazio su disco

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente hardware</th>
<th align="left">Requisito minimo</th>
<th align="left">Requisito consigliato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Responsabile del trattamento</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o superiore</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8 GB</p></td>
<td align="left"><p>12 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spazio disponibile su disco</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a>Requisiti per i database SQLServer

Nella tabella seguente sono elencate le versioni di SQLServer supportate per l'installazione delle funzionalità di amministrazione e monitoraggio del server, che include il database di ripristino, il database di conformità e di controllo e i report di conformità e controllo. I database richiedono inoltre l'installazione di strumenti di gestione di SQL Server.

**Nota**  MBAM non supporta nativamente il clustering SQL, il mirroring o i gruppi di disponibilità. Per installare i database, è necessario eseguire l'installazione di MBAM server in un server SQL autonomo.

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione di SQL Server</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftSQLServer2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftSQLServer2012</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente hardware</th>
<th align="left">Requisito minimo</th>
<th align="left">Requisito consigliato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Responsabile del trattamento</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o superiore</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8 GB</p></td>
<td align="left"><p>12 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spazio disponibile su disco</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB o superiore</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> Requisiti di sistema client di MBAM


### Requisiti del sistema operativo client

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del client e il monitoraggio dell'amministrazione di Microsoft BitLocker.

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
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Enterprise o Ultimate Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows To Go</p></td>
<td align="left"><p>Windows 8 Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a>Requisiti di RAM client

Non sono previsti requisiti di RAM specifici dell'installazione del client di amministrazione e monitoraggio di Microsoft BitLocker.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> Requisiti di sistema per i criteri di gruppo di MBAM


Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del modello di criteri di gruppo di amministrazione e monitoraggio di Microsoft BitLocker.

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
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Enterprise o Ultimate Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Versione standard o Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Pianificazione della distribuzione di MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Prerequisiti per la distribuzione di MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





