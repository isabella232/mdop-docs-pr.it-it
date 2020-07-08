---
title: Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server
description: Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815866"
---
# Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server


Se si vuole usare Application Virtualization Streaming Servers in combinazione con l'implementazione basata su Application Virtualization Management Server, è possibile scegliere tra diverse alternative, sfruttando qualsiasi infrastruttura già in vigore. Se ad esempio sono già presenti server nelle succursali dei campi, è possibile inserire la condivisione di Application Virtualization \\CONTENT su tali server e quindi configurare i client per l'uso di tale condivisione di contenuto come origine di contenuto dell'applicazione. Se si sceglie di usare solo i server di gestione della virtualizzazione delle applicazioni, ad esempio perché si ha una sola sede, i client possono eseguire lo streaming del contenuto da tale server.

Le opzioni supportate includono l'uso di un file server, di un server IIS o di un Application Virtualization Streaming Server. È anche possibile installare Application Virtualization Streaming Server in un file server o un server IIS esistente. Le caratteristiche di queste diverse opzioni sono riepilogate nella tabella seguente.

**Nota**  La funzionalità di aggiornamento attivo consente di aggiungere una nuova versione di un'applicazione a un server di gestione di App-V o a un server di flusso senza influire sugli utenti che stanno attualmente eseguendo l'applicazione. I client App-V riceveranno automaticamente la versione più recente dell'applicazione dall'App-V Management Server o dal server di streaming la volta successiva che l'utente avvia l'applicazione. Per questa caratteristica è necessario usare il protocollo RTSP (S).

 

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
<td align="left"><p>SMB</p></td>
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
<li><p>Supporta la sicurezza avanzata con il protocollo HTTPS</p></li>
<li><p>Supporta lo streaming in computer remoti su Internet</p></li>
<li><p>Aprire una sola porta nel firewall</p></li>
<li><p>Scalabile</p></li>
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
<li><p>Aprire una sola porta nel firewall</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Infrastruttura duale</p></li>
<li><p>Requisito di amministrazione del server</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)">Come configurare Application Virtualization Streaming Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Application Virtualization Management Server</p></td>
<td align="left"><p>RTSP/RTSPS</p></td>
<td align="left"><ul>
<li><p>Aggiornamento attivo</p></li>
<li><p>Supporta la sicurezza avanzata tramite il protocollo RTSPs</p></li>
<li><p>Aprire una sola porta nel firewall</p></li>
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


[Scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Panoramica dei componenti del sistema Application Virtualization](overview-of-the-application-virtualization-system-components.md)

[Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





