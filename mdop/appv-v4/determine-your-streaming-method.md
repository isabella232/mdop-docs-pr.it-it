---
title: Determinare il metodo di streaming
description: Determinare il metodo di streaming
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821666"
---
# Determinare il metodo di streaming


La prima volta che un utente fa doppio clic sull'icona inserita in un computer tramite il processo di pubblicazione, l'Application Virtualization Client otterrà il contenuto del pacchetto dell'applicazione virtuale da una posizione di origine di flusso.

**Nota** 
 Il *flusso* è il termine usato per descrivere il processo di ottenimento del contenuto da un pacchetto di applicazione sequenziata, a partire dal blocco di funzionalità principale e quindi ottenendo blocchi aggiuntivi in base alle esigenze.

 

La posizione di origine del flusso è in genere un server accessibile dal computer dell'utente; Tuttavia, alcuni sistemi di distribuzione elettronica, come Microsoft endpoint Configuration Manager, possono distribuire il file SFT nel computer dell'utente e quindi eseguire il flusso del pacchetto dell'applicazione virtuale localmente dalla cache di tale computer.

**Nota**  Una posizione di origine di flusso per i pacchetti virtuali può essere configurata in un computer che non è un server. Ciò è particolarmente utile in una piccola filiale che non ha un server.

 

Le origini di flusso che possono essere usate per archiviare le applicazioni sequenziate sono descritte nella tabella seguente.

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
<th align="left">Tipo di server</th>
<th align="left">Protocollo</th>
<th align="left">Vantaggi</th>
<th align="left">Svantaggi</th>
<th align="left">Collegamenti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>File server</p></td>
<td align="left"><p>File</p></td>
<td align="left"><ul>
<li><p>Soluzione semplice a basso costo per configurare il file server esistente con la condivisione di \CONTENT</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Nessun aggiornamento attivo</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)">Come configurare il file server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Server IIS</p></td>
<td align="left"><p>HTTP/HTTPS</p></td>
<td align="left"><ul>
<li><p>Supporta la sicurezza avanzata usando il protocollo HTTPS.</p></li>
<li><p>Supporta lo streaming in computer remoti su Internet</p></li>
<li><p>Aprire una sola porta nel firewall</p></li>
<li><p>Altamente scalabile</p></li>
<li><p>Protocollo familiare</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Necessità di gestire IIS</p></li>
<li><p>Nessun aggiornamento attivo</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)">Come configurare il server per IIS</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Application Virtualization Streaming Server</p></td>
<td align="left"><p>RTSP/RTSPS</p></td>
<td align="left"><ul>
<li><p>Aggiornamento attivo</p></li>
<li><p>Supporta la sicurezza avanzata tramite il protocollo RTSPs</p></li>
<li><p>Solo una porta nel firewall per l'apertura (solo RTSPs)</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Infrastruttura duale</p></li>
<li><p>Requisito di amministrazione del server</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Come configurare i server di gestione di Application Virtualization</a></p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario.md)

[Panoramica di uno scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario-overview.md)

[Determinare il metodo di pubblicazione](determine-your-publishing-method.md)

 

 





