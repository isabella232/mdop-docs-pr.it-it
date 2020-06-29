---
title: Panoramica dei componenti del sistema Application Virtualization
description: Panoramica dei componenti del sistema Application Virtualization
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816055"
---
# Panoramica dei componenti del sistema Application Virtualization


La tabella seguente descrive i componenti principali di Microsoft Application Virtualization Management System. Per altre informazioni sulla distribuzione di questi componenti di sistema, Vedi [scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente</th>
<th align="left">Funzione</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Management Server</p></td>
<td align="left"><p>Il componente responsabile per lo streaming del contenuto del pacchetto e la pubblicazione dei collegamenti e delle associazioni di tipi di file nel client di virtualizzazione dell'applicazione.</p></td>
<td align="left"><p>L'Application Virtualization Management Server supporta l'aggiornamento attivo, la gestione delle licenze e un database che può essere usato per la creazione di report.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong></strong>Cartella contenuto</p></td>
<td align="left"><p>Posizione dei pacchetti di virtualizzazione dell'applicazione per lo streaming.</p></td>
<td align="left"><p>Questa cartella può essere posizionata in una condivisione inserita o disattivata dall'Application Virtualization Management Server. La cartella può essere posizionata anche in una rete di archiviazione (SAN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Management Console</p></td>
<td align="left"><p>Un'utilità di gestione degli snap-in MMC 3,0 per l'amministrazione di Microsoft Application Virtualization Server.</p></td>
<td align="left"><p>Questo componente può essere installato nel server Microsoft Application Virtualization o posizionato in una workstation separata con MMC 3.0 e. NET 2.0 installato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servizio Web Microsoft Application Virtualization Management</p></td>
<td align="left"><p>Il componente responsabile per comunicare eventuali richieste di lettura/scrittura all'archivio dati di virtualizzazione dell'applicazione.</p></td>
<td align="left"><p>Questo componente può essere installato nel server Microsoft Application Virtualization o in un computer separato con IIS installato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Archivio dati di Microsoft Application Virtualization</p></td>
<td align="left"><p>Il componente archiviato nel database SQL e responsabile dell'archiviazione di tutte le informazioni relative all'infrastruttura di virtualizzazione dell'applicazione.</p></td>
<td align="left"><p>Queste informazioni includono tutti i record delle applicazioni, le assegnazioni delle applicazioni e i gruppi che hanno la responsabilità di gestire l'ambiente di virtualizzazione dell'applicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization Streaming Server</p></td>
<td align="left"><p>Il componente responsabile dell'hosting dei pacchetti di virtualizzazione dell'applicazione per il flusso di lavoro ai client in una filiale, in cui il collegamento all'Application Virtualization Management Server è considerato un WAN.</p></td>
<td align="left"><p>Questo server contiene solo funzionalità di flusso e non fornisce né l'Application Virtualization Management Console né il servizio Web Application Virtualization Management.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Sequencer</p></td>
<td align="left"><p>Il componente usato per monitorare e acquisire l'installazione di applicazioni per creare pacchetti di applicazioni virtuali.</p></td>
<td align="left"><p>L'output è costituito dalle icone dell'applicazione, da un file OSD che contiene informazioni sulla definizione del pacchetto, da un file manifesto del pacchetto e dal file SFT che contiene i file di contenuto del programma applicativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization Client</p></td>
<td align="left"><p>Il componente installato nel client Desktop Application Virtualization o nel client di virtualizzazione dell'applicazione per Servizi Desktop remoto (in precedenza Servizi terminal) e che fornisce l'ambiente virtuale per le applicazioni virtualizzate.</p></td>
<td align="left"><p>Il client Microsoft Application Virtualization gestisce il flusso del pacchetto in cache, aggiornamento della pubblicazione, trasporto e tutte le interazioni con i server di virtualizzazione dell'applicazione.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





