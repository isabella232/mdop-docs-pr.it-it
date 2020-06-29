---
title: Panoramica di Application Virtualization
description: Panoramica di Application Virtualization
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816065"
---
# Panoramica di Application Virtualization


Microsoft Application Virtualization (App-V) può rendere le applicazioni disponibili per i computer degli utenti finali senza dover installare le applicazioni direttamente in tali computer. Ciò viene reso possibile tramite un processo noto come *sequenziamento dell'applicazione*, che consente l'esecuzione di ogni applicazione nel proprio ambiente virtuale autonomo nel computer client. Le applicazioni sequenziate vengono isolate l'una dall'altra. In questo articolo vengono eliminati i conflitti di applicazione, ma le applicazioni possono comunque interagire con il computer client.

Il client App-V è la caratteristica che consente all'utente finale di interagire con le applicazioni dopo che sono state pubblicate nel computer. Il client gestisce l'ambiente virtuale in cui vengono eseguite le applicazioni virtualizzate in ogni computer. Dopo l'installazione del client in un computer, le applicazioni devono essere messe a disposizione del computer tramite un processo noto come *pubblicazione*, che consente all'utente finale di eseguire le applicazioni virtuali. Il processo di pubblicazione copia le icone e i tasti di scelta rapida dell'applicazione virtuale nel computer, in genere nel desktop di Windows o nel menu **Start** , e copia anche le informazioni di associazione per la definizione del pacchetto e il tipo di file nel computer. La pubblicazione rende inoltre disponibile il contenuto del pacchetto dell'applicazione per il computer dell'utente finale.

Il contenuto del pacchetto dell'applicazione virtuale può essere copiato in uno o più server di virtualizzazione dell'applicazione in modo che possa essere trasmesso ai client su richiesta e memorizzato nella cache localmente. I server di file e i server Web possono essere usati anche come server di streaming oppure il contenuto può essere copiato direttamente nel computer dell'utente finale, ad esempio se si usa un sistema di distribuzione del software elettronico, come Microsoft endpoint Configuration Manager. In un'implementazione multiserver, il mantenimento del contenuto del pacchetto e la sua conservazione aggiornata in tutti i server di flusso richiedono una soluzione di gestione dei pacchetti completa. A seconda delle dimensioni dell'organizzazione, potrebbe essere necessario disporre di molte applicazioni virtuali disponibili per gli utenti finali dislocate in tutto il mondo. La gestione dei pacchetti per garantire che le applicazioni appropriate siano disponibili per tutti gli utenti dove e quando è necessario accedervi è quindi un requisito importante.

## Funzionalità di Microsoft Application Virtualization System


La tabella seguente descrive le caratteristiche principali di Microsoft Application Virtualization Management System.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Funzionalità</th>
<th align="left">Funzione</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Management Server</p></td>
<td align="left"><p>Responsabile dello streaming del contenuto del pacchetto e della pubblicazione dei collegamenti e delle associazioni di tipi di file al client di Application Virtualization.</p></td>
<td align="left"><p>L'Application Virtualization Management Server supporta l'aggiornamento attivo, la gestione delle licenze e un database che può essere usato per la creazione di report.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong></strong>Cartella contenuto</p></td>
<td align="left"><p>Indica la posizione dei pacchetti di virtualizzazione dell'applicazione per il flusso.</p></td>
<td align="left"><p>Questa cartella può essere posizionata in una condivisione inserita o disattivata dall'Application Virtualization Management Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Management Console</p></td>
<td align="left"><p>Questa console è uno strumento di gestione dello snap-in MMC 3,0 usato per l'amministrazione di Microsoft Application Virtualization Server.</p></td>
<td align="left"><p>Questo strumento può essere installato nel server di Microsoft Application Virtualization o in una workstation separata che include Microsoft Management Console (MMC) 3.0 e Microsoft. NETFramework 2,0 installato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servizio Web Microsoft Application Virtualization Management</p></td>
<td align="left"><p>Responsabile della comunicazione delle richieste di lettura e scrittura all'archivio dati di virtualizzazione dell'applicazione.</p></td>
<td align="left"><p>Il servizio Web di gestione può essere installato nel server Microsoft Application Virtualization Management o in un computer separato in cui è installato Microsoft Internet Information Services (IIS).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Archivio dati di Microsoft Application Virtualization</p></td>
<td align="left"><p>Database di SQL Server App-V responsabile dell'archiviazione di tutte le informazioni relative all'infrastruttura di virtualizzazione dell'applicazione.</p></td>
<td align="left"><p>Queste informazioni includono tutti i record delle applicazioni, le assegnazioni delle applicazioni e i gruppi che hanno la responsabilità di gestire l'ambiente di virtualizzazione dell'applicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization Streaming Server</p></td>
<td align="left"><p>Responsabile dell'hosting dei pacchetti Application Virtualization per lo streaming ai client in una filiale, in cui il collegamento all'Application Virtualization Management Server è considerato una connessione WAN (Wide Area Networks).</p></td>
<td align="left"><p>Questo server contiene solo funzionalità di flusso e non fornisce né l'Application Virtualization Management Console né il servizio Web Application Virtualization Management.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Sequencer</p></td>
<td align="left"><p>Il sequencer viene usato per monitorare e acquisire l'installazione di applicazioni per creare pacchetti di applicazioni virtuali.</p></td>
<td align="left"><p>L'output è costituito dalle icone dell'applicazione, un file con estensione OSD che contiene informazioni sulla definizione del pacchetto, un file manifesto del pacchetto e il file SFT che contiene i file di contenuto del programma applicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization Client</p></td>
<td align="left"><p>Il client Desktop Application Virtualization e il client di Application Virtualization per Servizi Desktop remoto consentono di gestire l'ambiente virtuale per le applicazioni virtualizzate.</p></td>
<td align="left"><p>Il client Microsoft Application Virtualization gestisce il flusso del pacchetto in cache, aggiornamento della pubblicazione, trasporto e tutte le interazioni con i server di virtualizzazione dell'applicazione.</p></td>
</tr>
</tbody>
</table>

 

 

 





