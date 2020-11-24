---
title: Configurazioni supportate di MBAM 2.5
description: Configurazioni supportate di MBAM 2.5
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 8ed7915e33c5e4735a7c58674ed5f7d6da8e9a06
ms.sourcegitcommit: 9087f0a1b5bd3f81a9b790d5e39fdf39c18a2411
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182928"
---
# Configurazioni supportate di MBAM 2.5


È possibile eseguire Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 in una topologia autonoma o in una topologia di integrazione di Configuration Manager che si integra con MBAM con System Center Configuration Manager. Se si usa la configurazione consigliata per una topologia in un ambiente di produzione, MBAM supporta fino a 500.000 client MBAM. Per informazioni sull'architettura e le funzionalità consigliate configurate in ogni server per ogni topologia, vedere [architettura di alto livello per MBAM 2,5](high-level-architecture-for-mbam-25.md).

Per altre configurazioni specifiche della topologia di integrazione di Configuration Manager, vedere [versioni di Configuration Manager supportate da mbam](#bkmk-cm-ramreqs).

**Nota**  
Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita. Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.



## Lingue supportate da MBAM


Le tabelle seguenti mostrano le lingue supportate per il client MBAM (incluso il portale Self-Service) e il server MBAM in MBAM 2,5 e MBAM 2,5 SP1.

**Lingue supportate in MBAM 2,5 SP1:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Lingue client</th>
<th align="left">Lingue del server</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ceco (Repubblica Ceca) CS-CZ</p>
<p>Danese (Danimarca) da-DK</p>
<p>Olandese (Paesi Bassi) nl-NL</p>
<p>Inglese (Stati Uniti) en-US</p>
<p>Fi-FI Finlandese (Finlandia)</p>
<p>Francese (Francia) fr-FR</p>
<p>Tedesco (Germania) de-DE</p>
<p>Greco (Grecia) el-GR</p>
<p>Ungherese (Ungheria) hu-HU</p>
<p>Italiano (Italia) it-IT</p>
<p>Giapponese (Giappone) ja-JP</p>
<p>Coreano (Corea) ko-KR</p>
<p>Norvegese, Bokmål (Norvegia) nb-NO</p>
<p>Polacco (Polonia) PL-PL</p>
<p>Portoghese (Brasile) PT-BR</p>
<p>Portoghese (Portogallo) PT-PT</p>
<p>Russo (Russia) ru-RU</p>
<p>Slovacco (Slovacchia) SK-SK</p>
<p>Spagnolo (Spagna) es-ES</p>
<p>Svedese (Svezia) SV-SE</p>
<p>Turco (Turchia) tr-TR</p>
<p>Sloveno (Slovenia) SL-SI</p>
<p>Zh-CN (cinese semplificato)</p>
<p>Cinese tradizionale (Taiwan) ZH-TW</p></td>
<td align="left"><ul>
<li><p>Inglese (Stati Uniti) en-US</p></li>
<li><p>Francese (Francia) fr-FR</p></li>
<li><p>Tedesco (Germania) de-DE</p></li>
<li><p>Italiano (Italia) it-IT</p></li>
<li><p>Giapponese (Giappone) ja-JP</p></li>
<li><p>Coreano (Corea) ko-KR</p></li>
<li><p>Portoghese (Brasile) PT-BR</p></li>
<li><p>Russo (Russia) ru-RU</p></li>
<li><p>Spagnolo (Spagna) es-ES</p></li>
<li><p>Zh-CN (cinese semplificato)</p></li>
<li><p>Cinese tradizionale (Taiwan) ZH-TW</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Lingue supportate in MBAM 2,5:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Lingue client</th>
<th align="left">Lingue del server</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>Inglese (Stati Uniti) en-US</p></li>
<li><p>Francese (Francia) fr-FR</p></li>
<li><p>Tedesco (Germania) de-DE</p></li>
<li><p>Italiano (Italia) it-IT</p></li>
<li><p>Giapponese (Giappone) ja-JP</p></li>
<li><p>Coreano (Corea) ko-KR</p></li>
<li><p>Portoghese (Brasile) PT-BR</p></li>
<li><p>Russo (Russia) ru-RU</p></li>
<li><p>Spagnolo (Spagna) es-ES</p></li>
<li><p>Zh-CN (cinese semplificato)</p></li>
<li><p>Cinese tradizionale (Taiwan) ZH-TW</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Inglese (Stati Uniti) en-US</p></li>
<li><p>Francese (Francia) fr-FR</p></li>
<li><p>Tedesco (Germania) de-DE</p></li>
<li><p>Italiano (Italia) it-IT</p></li>
<li><p>Giapponese (Giappone) ja-JP</p></li>
<li><p>Coreano (Corea) ko-KR</p></li>
<li><p>Portoghese (Brasile) PT-BR</p></li>
<li><p>Russo (Russia) ru-RU</p></li>
<li><p>Spagnolo (Spagna) es-ES</p></li>
<li><p>Zh-CN (cinese semplificato)</p></li>
<li><p>Cinese tradizionale (Taiwan) ZH-TW</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> Requisiti di sistema di MBAM server


### Requisiti del sistema operativo di MBAM server

Ti consigliamo vivamente di eseguire il client MBAM e il server MBAM sulla stessa linea di sistemi operativi. Ad esempio, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2 e così via.

La tabella seguente elenca i sistemi operativi supportati per l'installazione di MBAM server.

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
<td align="left"><p>Windows Server 2019</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, aziendale o Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>



Il dominio aziendale deve contenere almeno un controller di dominio di Windows Server 2008 (o versioni successive).

### <a href="" id="bkmk-stand-alone-ramreqs"></a>Requisiti per il processore, la RAM e lo spazio su disco di MBAM server-topologia autonoma

Questi requisiti sono per la topologia autonoma di MBAM. Per i requisiti della topologia di integrazione di Configuration Manager, vedi la topologia di integrazione di gestione configurazione, per i requisiti di [Disk Processor, RAM e spazio su disco](#bkmk-cm-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento hardware</th>
<th align="left">Requisito minimo</th>
<th align="left">Requisito consigliato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processore</p></td>
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



### <a href="" id="bkmk-cm-ramreqs"></a>Requisiti per il processore, la RAM e lo spazio su disco di MBAM server-topologia di integrazione di Configuration Manager

Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco per i server MBAM quando si usa la topologia di integrazione di Configuration Manager. Per i requisiti per la topologia autonoma, vedere [requisiti per il processore, la RAM e lo spazio su disco di mbam server-topologia](#bkmk-stand-alone-ramreqs)autonoma.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento hardware</th>
<th align="left">Requisito minimo</th>
<th align="left">Requisito consigliato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processore</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o superiore</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spazio disponibile su disco</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a>Versioni di Configuration Manager supportate da MBAM

MBAM supporta le versioni seguenti di Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione supportata</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (Current Branch), versioni fino a 1902</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 1806</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (LTSB-versione 1606)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestione configurazione di Microsoft System Center 2012</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2 o versioni successive</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p>

&gt;<strong>Nota </strong> anche se Configuration Manager 2007 R2 è 32 bit, è necessario installarlo e SQL Server in un sistema operativo a 64 bit per far corrispondere il software mbam a 64 bit.
</td>
</tr>
</tbody>
</table>



Per un elenco delle configurazioni supportate per il Server Configuration Manager, vedere la documentazione appropriata di TechNet per la versione di Configuration Manager in uso. MBAM non ha requisiti di sistema aggiuntivi per il Server Configuration Manager.

### <a href="" id="sql-server-database-requirements-"></a>Requisiti di database di SQL Server

Nella tabella seguente sono elencate le versioni di Microsoft SQL Server supportate per le funzionalità di MBAM server, che includono il database di ripristino, la conformità e il database di audit e la caratteristica report. Le versioni necessarie si applicano alle topologie di integrazione autonoma o Gestione configurazione.

È necessario installare SQL Server con **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** regole di confronto.

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
<td align="left"><p>Microsoft SQL Server 2019</p></td>
<td align="left"><p>Standard, aziendale o Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p></td><br/><tr class="even">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p>Standard, aziendale o Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p></td><br/><tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>Standard, aziendale o Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p>64 bit</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>Standard, aziendale o Datacenter</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64 bit</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>Standard, aziendale o Datacenter</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>64 bit</p></td>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>Standard o Enterprise</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>

**Nota**  
MBAM ha un livello di compatibilità supportato massimo di 140. Il livello di compatibilità predefinito per i nuovi database creati in SQL Server 2019 è 150 che deve essere modificato in 140 o inferiore, usando il comando ALTER DATABASE, dopo la creazione del database. I database esistenti migrati da SQL Server 2017 o inferiore rimarranno al livello di compatibilità precedente e non devono essere modificati.

Per supportare SQL 2016, è necessario installare la versione di manutenzione di marzo 2017 per MDOP https://www.microsoft.com/download/details.aspx?id=54967  e per supportare sql 2017 è necessario installare la versione di manutenzione di luglio 2018 per MDOP https://www.microsoft.com/download/details.aspx?id=57157 . In generale, è possibile usare sempre l'aggiornamento della manutenzione più recente, poiché include anche tutti i bug e le nuove caratteristiche.


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a>Requisiti di spazio per processori, RAM e spazi su disco di SQL Server-topologia autonoma

Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco consigliati per il computer SQL Server quando si usa la topologia autonoma. Usare questi requisiti come guida. I requisiti specifici variano in base al numero di computer client supportati nell'organizzazione. Per visualizzare i requisiti per la topologia di integrazione di Configuration Manager, vedere [requisiti relativi a SQL Server Processor, RAM e spazio su disco-topologia di integrazione di Configuration Manager](#bkmk-cm-sql-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento hardware</th>
<th align="left">Requisito minimo</th>
<th align="left">Requisito consigliato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processore</p></td>
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



### <a href="" id="bkmk-cm-sql-ramreqs"></a>Requisiti di spazio su processori, RAM e Space disk per SQL Server-topologia di integrazione di Configuration Manager

Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco del server per il computer Microsoft SQL Server quando si usa la topologia di integrazione di Configuration Manager, vedere Requisiti per la [topologia autonoma di processori, RAM e spazio su disco di SQL Server](#bkmk-sql-stand-alone-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento hardware</th>
<th align="left">Requisito minimo</th>
<th align="left">Requisito consigliato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processore</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o superiore</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spazio disponibile su disco</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> Requisiti di sistema client di MBAM


### Requisiti del sistema operativo client

Ti consigliamo vivamente di eseguire il client MBAM e il server MBAM sulla stessa linea di sistemi operativi. Ad esempio, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2 e così via.

La tabella seguente elenca i sistemi operativi supportati per l'installazione di MBAM client. Gli stessi requisiti si applicano alle topologie di integrazione autonoma e gestione configurazione.

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
<tr class="even">
    <td align="left"><p>Windows 10</p></td>
    <td align="left"><p>Funzionalità per le aziende</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p>32 o 64 bit</p></td>
</tr><br/><tr class="odd">
<td align="left"><p>Windows10</p></td>
<td align="left"><p>Funzionalità per le aziende</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Funzionalità per le aziende</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Enterprise o Ultimate</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows To Go</p></td>
<td align="left"><p>Windows 8,1 e Windows 10 Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Requisiti di RAM client

Non ci sono requisiti di RAM specifici per l'installazione del client MBAM.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> Requisiti di sistema per i criteri di gruppo di MBAM


La tabella seguente elenca i sistemi operativi supportati per l'installazione dei modelli di criteri di gruppo di MBAM.

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
 <tr class="even">
      <td align="left"><p>Windows 10</p></td>
      <td align="left"><p>Funzionalità per le aziende</p></td>
      <td align="left"><p></p></td>
      <td align="left"><p>32 o 64 bit</p></td>
 </tr>
<tr class="odd">
<td align="left"><p>Windows10</p></td>
<td align="left"><p>Funzionalità per le aziende</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Funzionalità per le aziende</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Enterprise o Ultimate</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, aziendale o Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>

## MBAM in Azure IaaS

Il server MBAM può essere distribuito in un'infrastruttura di Azure come servizio (IaaS) in una delle versioni supportate del sistema operativo elencate sopra, che si connettono a una directory ospitata in locale o in Active Directory ospitata anche in Azure IaaS.  La documentazione relativa alla configurazione e alla configurazione di Active Directory in Azure IaaS è disponibile [qui](https://msdn.microsoft.com/library/azure/jj156090.aspx).

Il client MBAM non è supportato nelle macchine virtuali e non è supportato anche in Azure IaaS.


## Versioni di servizio 

- [Hotfix 2016 aprile](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [2016 settembre](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [Dicembre 2016](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [Marzo 2017](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [Giugno 2017](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [Settembre 2017](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [Marzo 2018](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [2018 luglio](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [2019 maggio](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## Argomenti correlati


[Pianificazione della distribuzione di MBAM 2.5](planning-to-deploy-mbam-25.md)

[Preparazione dell'ambiente per MBAM 2.5](preparing-your-environment-for-mbam-25.md)




## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




