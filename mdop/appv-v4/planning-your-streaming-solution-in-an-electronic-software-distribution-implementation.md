---
title: Pianificazione della soluzione di streaming in un'implementazione della distribuzione elettronica del software
description: Pianificazione della soluzione di streaming in un'implementazione della distribuzione elettronica del software
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815856"
---
# Pianificazione della soluzione di streaming in un'implementazione della distribuzione elettronica del software


Se si decide di usare i server di streaming in combinazione con il sistema ESD per rendere disponibile il contenuto dell'applicazione per i computer degli utenti finali, è possibile scegliere tra diverse alternative, sfruttando qualsiasi tipo di infrastruttura già in vigore. Ad esempio, se il sistema ESD include condivisioni di distribuzione del software nei server delle succursali dei campi, è possibile inserire la condivisione di Application Virtualization \\CONTENT su tali server e quindi configurare i client per l'uso della condivisione di contenuto come origine di contenuto dell'applicazione. Le opzioni supportate includono l'uso di un file server o di un server IIS. È anche possibile installare Application Virtualization Streaming Server in un file server o un server IIS esistente.

Application Virtualization Streaming Server offre il supporto per la funzionalità di aggiornamento attivo nella virtualizzazione delle applicazioni. La funzionalità di aggiornamento attivo consente di aggiungere una nuova versione di un'applicazione a un server di gestione di App-V o a un server di flusso senza influire sugli utenti che stanno attualmente eseguendo l'applicazione. I client App-V riceveranno automaticamente la versione più recente dell'applicazione dall'App-V Management Server o dal server di streaming la volta successiva che l'utente avvia l'applicazione. Per questa caratteristica è necessario usare il protocollo RTSP (S). Se si sceglie di non usare Application Virtualization Streaming Server, è necessario gestire in modo esplicito gli aggiornamenti dei pacchetti di applicazioni tramite il sistema ESD.

**Nota**  L'accesso alle applicazioni viene controllato tramite gruppi di sicurezza in servizi di dominio Active Directory, quindi sarà necessario pianificare un processo per la configurazione di un gruppo di sicurezza per ogni applicazione virtuale e per la gestione degli utenti aggiunti a ogni gruppo. L'amministratore dell'Application Virtualization System configura ogni server di flusso per l'uso di questi gruppi di Active Directory applicando gli elenchi ACL alle directory dell'applicazione sotto la condivisione di contenuto, che controlla l'accesso ai pacchetti in base all'appartenenza ai gruppi di Active Directory.

 

Le caratteristiche delle opzioni di flusso disponibili sono riepilogate nella tabella seguente.

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
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Come configurare i server di gestione di Application Virtualization</a></p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Come configurare i server per la distribuzione basata su ESD](how-to-configure-servers-for-esd-based-deployment.md)

[Panoramica di sicurezza e protezione](security-and-protection-overview.md)

[Pubblicazione delle applicazioni virtuali con distribuzione elettronica del software](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





