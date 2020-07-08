---
title: Configurazioni supportate di MBAM 1.0
description: Configurazioni supportate di MBAM 1.0
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825936"
---
# Configurazioni supportate di MBAM 1.0


Questo argomento specifica i requisiti necessari per installare ed eseguire l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) nell'ambiente.

## <a href="" id="---------mbam-server-system-requirements"></a> Requisiti di sistema di MBAM server


### Requisiti del sistema operativo del server

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di amministrazione e monitoraggio di Microsoft BitLocker.

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
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter o server Web</p></td>
<td align="left"><p>Solo SP2</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter o server Web</p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>



**Warning**  
Non è disponibile alcun supporto per l'installazione di servizi, report o database di MBAM in un computer controller di dominio.



### <a href="" id="server-random-access-memory--ram--requirements-"></a>Requisiti della RAM (Random Access Memory) del server

Non ci sono requisiti di RAM specifici per l'installazione di MBAM server.

### <a href="" id="sql-server-database-requirements-"></a>Requisiti di database di SQL Server

La tabella seguente elenca le versioni di SQL Server supportate per l'installazione delle funzionalità di MBAM server.

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
<th align="left">Funzionalità del server MBAM</th>
<th align="left">Versione di SQL Server</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Report di conformità e controllo</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, standard, Enterprise, Datacenter o Developer Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Database di ripristino e hardware</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Enterprise, Datacenter o Developer Edition</p>
<div class="alert">
<strong>Importante</strong><br/><p>Le edizioni standard di SQL Server non sono supportate per l'installazione delle funzionalità del server database hardware e ripristino di MBAM.</p>
</div>
<div>

</div></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Database di conformità e controllo</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, standard, Enterprise, Datacenter o Developer Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> Requisiti di sistema client di MBAM


### Requisiti del sistema operativo client

La tabella seguente elenca i sistemi operativi supportati per l'installazione di MBAM client.

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
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Enterprise Edition</p></td>
<td align="left"><p>Nessuno, SP1</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Ultimate Edition</p></td>
<td align="left"><p>Nessuno, SP1</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Requisiti di RAM client

Non ci sono requisiti di RAM specifici per l'installazione del client MBAM.

## Argomenti correlati


[Pianificazione della distribuzione di MBAM 1.0](planning-to-deploy-mbam-10.md)

[Prerequisiti per la distribuzione di MBAM 1.0](mbam-10-deployment-prerequisites.md)









