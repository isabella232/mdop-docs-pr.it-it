---
title: Configurazioni supportate di MED-V 1.0 SP1
description: Configurazioni supportate di MED-V 1.0 SP1
author: dansimp
ms.assetid: 4dcf37c4-a061-43d2-878c-28efc87c3cdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5a707e8a3d59a423308f9f735ff38df9e235fbf5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824166"
---
# Configurazioni supportate di MED-V 1.0 SP1


Questo argomento specifica i requisiti necessari per installare ed eseguire Microsoft Enterprise Desktop Virtualization (MED-V) 1,0 Service Pack 1 (SP1) nell'ambiente.

## Requisiti di sistema client di MED-V 1,0 SP1


### Requisiti del sistema operativo client MED-V

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del client MED-V 1,0 SP1.

**Nota**  
Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere [Service Pack supportati](https://go.microsoft.com/fwlink/?LinkId=31975) per il ciclo di vita ( https://go.microsoft.com/fwlink/?LinkId=31975) . Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/?LinkId=31976) di supporto del ciclo di vita del supporto Microsoft https://go.microsoft.com/fwlink/?LinkId=31976)



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
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP2 o SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise o Ultimate</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Professionale, aziendale o finale</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
</tbody>
</table>



**Nota**  
Il client MED-V non viene eseguito in modalità x64 nativa. Invece, MED-V viene eseguito in Windows in modalità Windows 64 bit (WOW64) in computer a 64 bit.



Nella tabella seguente sono elencate le RAM minime necessarie per ogni sistema operativo supportato in MED-V 1,0 SP1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">RAM obbligatoria minima</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows XP Professional</p></td>
<td align="left"><p>1 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 x86</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7 x64</p></td>
<td align="left"><p>3 GB</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-client-configuration-"></a>Configurazione client di MED-V 1,0 SP1

**Versione di .NET Framework**

Le versioni seguenti di Microsoft .NET Framework sono supportate per l'installazione del client MED-V 1,0 SP1:

-   .NET Framework 2,0 o .NET Framework 2,0 SP1

-   .NET Framework 3,0 o .NET Framework 3,0 SP1

-   .NET Framework 3,5 o .NET Framework 3,5 SP1

**Motore di virtualizzazione**

Microsoft Virtual PC 2007 SP1 con l'hotfix descritto nell'articolo della Microsoft Knowledge base 974918 è supportato per l'installazione del client MED-V 1,0 SP1 nelle configurazioni seguenti:

-   File del disco rigido virtuale statico (VHD)

-   Più file VHD che si trovano all'interno della stessa directory

-   File VHD dinamico

**Browser Internet**

Windows Internet Explorer 7 e Windows Internet Explorer 8 sono supportati per l'installazione del client MED-V 1,0 SP1.

**Microsoft Hyper-V Server**

Il client MED-V non è supportato in un ambiente server Microsoft Hyper-V.

## Requisiti di sistema per l'area di lavoro di MED-V 1,0 SP1


MED-V 1,0 SP1 introduce le modifiche ai requisiti di sistema da quelli per MED-V 1,0.

### Requisiti del sistema operativo per l'area di lavoro MED-V

Nella tabella seguente sono elencati i sistemi operativi supportati per le aree di lavoro di MED-V 1,0 SP1.

**Nota**  
Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere [Service Pack supportati](https://go.microsoft.com/fwlink/?LinkId=31975) per il ciclo di vita ( https://go.microsoft.com/fwlink/?LinkId=31975) . Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/?LinkId=31976) di supporto del ciclo di vita del supporto Microsoft https://go.microsoft.com/fwlink/?LinkId=31976)



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
<td align="left"><p>Windows 2000</p></td>
<td align="left"><p>Professional</p></td>
<td align="left"><p>SP4</p></td>
<td align="left"><p>X86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP2 o SP3</p>
<div class="alert">
<strong>Nota</strong><br/><p>È consigliabile usare SP3 per verificare che l'area di lavoro MED-V sia compatibile con le versioni future di MED-V.</p>
</div>
<div>

</div></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-workspace-configuration-"></a>Configurazione dell'area di lavoro di MED-V 1,0 SP1

**Versione di .NET Framework**

MED-V richiede una delle versioni supportate seguenti dell'installazione dell'area di lavoro di Microsoft .NET Framework per MED-V 1,0 SP1:

-   .NET Framework 2,0 SP1

-   .NET Framework 3,0 SP1

-   .NET Framework 3,5 o .NET Framework 3,5 SP1

**Nota**  
È consigliabile usare .NET Framework 3,5 SP1 per verificare che l'area di lavoro MED-V sia compatibile con le versioni future di MED-V.



**Browser Internet**

Windows Internet Explorer 6 SP2 e Windows Internet Explorer 7 sono supportati per l'installazione dell'area di lavoro MED-V 1,0 SP1.

### <a href="" id="med-v-workspace-images-"></a>Immagini dell'area di lavoro MED-V

Le immagini dell'area di lavoro MED-V devono essere create usando Virtual PC 2007 SP1.

## Requisiti di sistema server MED-V 1,0 SP1


MED-V 1,0 SP1 introduce le modifiche ai requisiti di sistema da quelli per MED-V 1,0.

### Requisiti del sistema operativo server MED-V 1,0

Nella tabella seguente sono elencati i sistemi operativi supportati per le installazioni del server MED-V 1,0 SP1.

**Nota**  
Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere [Service Pack supportati](https://go.microsoft.com/fwlink/?LinkId=31975) per il ciclo di vita ( https://go.microsoft.com/fwlink/?LinkId=31975) . Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/?LinkId=31976) di supporto del ciclo di vita del supporto Microsoft https://go.microsoft.com/fwlink/?LinkId=31976)



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
<td align="left"><p>Standard o Enterprise</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>X86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard o Enterprise</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-server-configuration-"></a>Configurazione del server MED-V 1,0 SP1

**Versione di .NET Framework**

MED-V richiede una delle versioni supportate seguenti dell'installazione dell'area di lavoro di Microsoft .NET Framework per MED-V 1,0 SP1:

-   .NET Framework 2,0 o .NET Framework 2,0 SP1

-   .NET Framework 3,0 o .NET Framework 3,0 SP1

-   .NET Framework 3,5 o .NET Framework 3,5 SP1

**Versione di Microsoft SQL Server**

Le versioni seguenti di Microsoft SQL Server sono supportate per MED-V 1,0 SP1 quando SQL Server viene installato localmente o in remoto dal server MED-V 1,0 SP1:

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
<td align="left"><p>SQL Server 2005</p></td>
<td align="left"><p>Express, standard o Enterprise Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>X86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server 2008</p></td>
<td align="left"><p>Express, standard o Enterprise</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>X86 o x64</p></td>
</tr>
</tbody>
</table>



**Microsoft Hyper-V Server**

Il server MED-V è supportato in un ambiente server Microsoft Hyper-V.

## Informazioni sulla globalizzazione di MED-V 1,0 SP1


Anche se MED-V non viene rilasciato in lingue diverse dall'inglese, sono supportate le seguenti versioni della lingua del sistema operativo Windows per il client, l'area di lavoro e le installazioni del server MED-V 1,0 SP1:

-   Inglese

-   Francese

-   Tedesco

-   Italiano

-   Spagnolo

-   Portoghese (Brasile)

-   Olandese (Paesi Bassi)

-   Giapponese









