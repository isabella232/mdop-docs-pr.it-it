---
title: Configurazioni supportate di MED-V 2.0
description: Configurazioni supportate di MED-V 2.0
author: dansimp
ms.assetid: 88f1d232-aa01-45ab-8da7-d086269250b5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0fed090ec04cf67a32b13533f4003c01ae167493
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825216"
---
# Configurazioni supportate di MED-V 2.0


L'ambiente può già soddisfare i requisiti di configurazione forniti in questo articolo, in modo da poter installare ed eseguire Microsoft Enterprise Desktop Virtualization (MED-V) 2,0. Sono stati inclusi requisiti tra cui il sistema operativo host, lo spazio su disco e i requisiti per l'area di lavoro MED-V.

## Requisiti del computer host MED-V 2.0


### Requisiti del sistema operativo host MED-V 2,0

Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione di MED-V 2,0 nel computer host.

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
<td align="left"><p>Professionale, aziendale o finale</p></td>
<td align="left"><p>Nessuno o SP1</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
</tbody>
</table>

 

Nella tabella seguente sono elencate le RAM minime necessarie per ogni sistema operativo supportato in MED-V 2,0.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">RAM minima richiesta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7 x86</p></td>
<td align="left"><p>2GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7 x64</p></td>
<td align="left"><p>2GB</p></td>
</tr>
</tbody>
</table>

 

### Spazio su disco consigliato minimo

È consigliabile un minimo di 10 GB di spazio di archiviazione disponibile. Lo spazio su disco richiesto, tuttavia, varia notevolmente e dipende dal numero di applicazioni pubblicate nell'area di lavoro MED-V.

### <a href="" id="med-v-2-0-host-configuration-"></a>Configurazione host MED-V 2.0

**Versione di .NET Framework**

La versione di .NET Framework 3.5 SP1 di Microsoft .NET Framework è necessaria per MED-V 2,0. Tuttavia, è possibile installare .NET Framework 4 o versione successiva se .NET Framework 3,5 è già installato.

**Motore di virtualizzazione**

Windows Virtual PCwith l'hotfix descritto nell'articolo 977206 della Microsoft Knowledge base è supportato per MED-V 2,0.

**Browser Internet**

Windows Internet Explorer8 e Windows Internet Explorer 9 sono supportati per MED-V 2,0.

**Ambienti Microsoft Server**

L'agente host MED-V e il Packager area di lavoro MED-V non sono supportati in qualsiasi ambiente server.

## Requisiti per l'area di lavoro MED-V 2.0


### Requisiti del sistema operativo MED-V 2,0 per l'area di lavoro

Nella tabella seguente sono elencati i sistemi operativi supportati per le aree di lavoro MED-V 2,0.

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
<td align="left"><p>SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="med-v-2-0-workspace-configuration-"></a>Configurazione dell'area di lavoro MED-V 2.0

**Versione di .NET Framework**

È supportata solo la versione di .NET Framework 3.5 SP1 di Microsoft .NET Framework per l'installazione di area di lavoro MED-V 2,0.

**Browser Internet**

Windows Internet Explorer6, Windows Internet Explorer7, Windows Internet Explorer8 e Windows Internet Explorer9 sono supportati per l'installazione dell'area di lavoro MED-V 2,0.

### Creazione di un'area di lavoro MED-V 2,0

Il disco rigido virtuale usato per creare un pacchetto di area di lavoro MED-V 2,0 deve essere creato tramite Windows Virtual PC.

## Informazioni sulla globalizzazione di MED-V 2,0


### Informazioni sulla globalizzazione dell'agente host MED-V 2,0

Le versioni della lingua del sistema operativo Windows seguenti sono supportate per l'agente host MED-V 2,0:

-   Francese

-   Italiano

-   Tedesco

-   Spagnolo

-   Coreano

-   Giapponese

-   Portoghese brasiliano

-   Russo

-   Cinese tradizionale

-   Cinese semplificato

-   Olandese

-   Svedese

-   Danese

-   Finlandese

-   Portoghese

-   Norvegese

-   Polacco

-   Turco

-   Ungherese

-   Ceco

-   Greco

-   Slovacco

-   Sloveno

### Informazioni sulla globalizzazione di Packager area di lavoro MED-V 2,0

Le versioni della lingua del sistema operativo Windows seguenti sono supportate per il Packager area di lavoro MED-V 2,0:

-   Francese

-   Italiano

-   Tedesco

-   Spagnolo

-   Coreano

-   Giapponese

-   Portoghese brasiliano

-   Russo

-   Cinese tradizionale

-   Cinese semplificato

## Argomenti correlati


[Distribuzione di MED-V](deployment-of-med-v.md)

 

 





