---
title: Scenari di server con connessione Internet per le reti perimetrali
description: Scenari di server con connessione Internet per le reti perimetrali
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816285"
---
# Scenari di server con connessione Internet per le reti perimetrali


App-V 4.5 supporta scenari server con accesso a Internet, in cui gli utenti che non sono connessi alla rete aziendale o che si disconnettono dalla rete possono ancora usare app-V. Come illustrato nella figura seguente, è supportato solo l'uso di protocolli protetti su Internet (RTSPs e HTTPS).

![diagramma di posizionamento del Firewall App-v](images/appvfirewalls.gif)

È possibile configurare una soluzione Internet, usando un server ISA, in cui l'infrastruttura App-V si trova nella rete interna nei modi seguenti:

-   Creare una regola di pubblicazione Web per il server IIS che ospita i file ICO e OSD, e facoltativamente i pacchetti per il flusso, che si trovano nella rete interna. Le procedure dettagliate sono disponibili in <https://go.microsoft.com/fwlink/?LinkId=151982> .

-   Creare una regola di pubblicazione del server per App-V Web Management Server (RTSPs). Le procedure dettagliate sono disponibili in [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .

Come illustrato nella figura seguente, se l'infrastruttura ha implementato altri firewall tra il client e il server ISA o tra ISA Server e la rete interna, è necessario creare regole del firewall RTSPs (TCP 322) e HTTPS (TCP 443) per supportare il flusso del traffico. Inoltre, se i firewall sono stati implementati tra ISA Server e la rete interna, il traffico predefinito necessario per i membri del dominio deve essere autorizzato a eseguire il tunneling attraverso il firewall (DNS, LDAP, Kerberos, SMB/CIFS).

![diagramma firewall di rete perimetrale App-v](images/appvperimeternetworkfirewall.gif)

Poiché le soluzioni firewall variano da ambiente a ambiente, le indicazioni fornite in questo argomento descrivono il traffico che sarebbe necessario per configurare un ambiente App-V con accesso a Internet nella rete perimetrale. Queste informazioni includono anche i server di rete interni consigliati.

Posizionare i server seguenti nella rete perimetrale:

-   App-V Management Server

-   Server IIS per la pubblicazione e lo streaming

**Nota**  Si consiglia di posizionare il server di gestione e IIS in computer separati.

 

Posizionare i server seguenti nella rete interna:

-   Content Server

-   Archivio dati (SQL Server)

-   Controller di dominio Active Directory

## Requisiti per il traffico


Le tabelle seguenti elencano i requisiti di traffico per la comunicazione da Internet e dalla rete perimetrale e dalla rete perimetrale alla rete interna.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisiti per il traffico da Internet alla rete perimetrale</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>RTSPs (aggiornamento della pubblicazione e pacchetti di flusso)</p></td>
<td align="left"><p>TCP 322 per impostazione predefinita; Questa operazione può essere modificata in App-V Management Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>HTTPS (Publishing ICO e file OSD e pacchetti di flusso)</p></td>
<td align="left"><p>TCP 443 per impostazione predefinita; Questa operazione può essere modificata nella configurazione di IIS.</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisiti per il traffico dalla rete perimetrale alla rete interna</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL Server</p></td>
<td align="left"><p>TCP 1433 è l'impostazione predefinita, ma può essere configurata in SQL Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SMB/CIFS</p></td>
<td align="left"><p>Se la directory di contenuto si trova in remoto dal server di gestione o dal server IIS (scelta consigliata).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kerberos</p></td>
<td align="left"><p>TCP e UDP 88</p></td>
</tr>
<tr class="even">
<td align="left"><p>LDAP</p></td>
<td align="left"><p>TCP e UDP 389</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DNS</p></td>
<td align="left"><p>Per la risoluzione dei nomi delle risorse interne (può essere eliminata con l'uso del file dell'host nei server di rete perimetrale)</p></td>
</tr>
</tbody>
</table>

 

 

 





