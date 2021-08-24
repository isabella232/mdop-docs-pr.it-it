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
ms.openlocfilehash: 7415cf7a97edc646653df552723667bac8d25fdc
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910691"
---
# <a name="internet-facing-server-scenarios-for-perimeter-networks"></a>Scenari di server con connessione Internet per le reti perimetrali


App-V 4.5 supporta scenari server con connessione Internet, in cui gli utenti che non sono connessi alla rete aziendale o che si disconnettino dalla rete possono comunque usare App-V. Come illustrato nella figura seguente, è supportato solo l'utilizzo di protocolli sicuri su Internet (RTSPS e HTTPS).

![Diagramma di posizionamento del firewall app-v.](images/appvfirewalls.gif)

È possibile configurare una soluzione con connessione Internet utilizzando un server ISA, in cui l'infrastruttura App-V si trova nella rete interna nei modi seguenti:

-   Creare una regola di pubblicazione Web per il server IIS che ospita i file ICO e OSD e, facoltativamente, i pacchetti per lo streaming, che si trovano nella rete interna. La procedura dettagliata è disponibile all'indirizzo <https://go.microsoft.com/fwlink/?LinkId=151982> .

-   Creare una regola di pubblicazione server per il server di gestione Web App-V (RTSPS). La procedura dettagliata è disponibile all'indirizzo [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .

Come illustrato nella figura seguente, se l'infrastruttura ha implementato altri firewall tra il client e ISA Server o tra ISA Server e la rete interna, è necessario creare regole firewall RTSPS (TCP 322) e HTTPS (TCP 443) per supportare il flusso di traffico. Inoltre, se sono stati implementati firewall tra ISA Server e la rete interna, il traffico predefinito necessario per i membri del dominio deve essere autorizzato a eseguire il tunneling attraverso il firewall (DNS, LDAP, Kerberos, SMB/CIFS).

![Diagramma del firewall della rete perimetrale app-v.](images/appvperimeternetworkfirewall.gif)

Poiché le soluzioni firewall variano da ambiente a ambiente, le indicazioni fornite in questo argomento descrivono il traffico necessario per configurare un ambiente App-V con connessione Internet nella rete perimetrale. Queste informazioni includono anche i server di rete interni consigliati.

Posizionare i server seguenti nella rete perimetrale:

-   Server di gestione App-V

-   Server IIS per la pubblicazione e lo streaming

**Nota**  
È consigliabile posizionare il server di gestione e il server IIS in computer distinti.

 

Posizionare i server seguenti nella rete interna:

-   Content server

-   Archivio dati (SQL Server)

-   Controller di dominio Active Directory

## <a name="traffic-requirements"></a>Requisiti relativi al traffico


Nelle tabelle seguenti sono elencati i requisiti di traffico per le comunicazioni da Internet e dalla rete perimetrale e dalla rete perimetrale alla rete interna.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisiti di traffico da Internet alla rete perimetrale</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>RTSPS (pubblicazione di pacchetti di aggiornamento e streaming)</p></td>
<td align="left"><p>TCP 322 per impostazione predefinita; questo può essere modificato in App-V Management Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>HTTPS (pubblicazione di file ICO e OSD e pacchetti di streaming)</p></td>
<td align="left"><p>TCP 443 per impostazione predefinita; questo può essere modificato nella configurazione di IIS.</p></td>
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
<th align="left">Requisiti di traffico dalla rete perimetrale alla rete interna</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL Server</p></td>
<td align="left"><p>TCP 1433 è il valore predefinito, ma può essere configurato in SQL Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SMB/CIFS</p></td>
<td align="left"><p>Se la directory del contenuto si trova in remoto dal server di gestione o dal server IIS (scelta consigliata).</p></td>
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
<td align="left"><p>Per la risoluzione dei nomi delle risorse interne (può essere eliminato con l'uso del file dell'host nei server della rete perimetrale)</p></td>
</tr>
</tbody>
</table>

 

 

 





