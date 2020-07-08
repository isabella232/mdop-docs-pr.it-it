---
title: Architettura di alto livello per App-V 5.0
description: Architettura di alto livello per App-V 5.0
author: dansimp
ms.assetid: fdf8b841-918f-4672-b352-0f2b9519581b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0ec105ffcc3213e488615603484b2de6bafce4d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805817"
---
# Architettura di alto livello per App-V 5.0


Usare le informazioni seguenti per semplificare la distribuzione di Microsoft Application Virtualization (App-V) 5,0.

## Panoramica dell'architettura


Un'implementazione tipica di App V 5,0 è costituita dagli elementi seguenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 Management Server</p></td>
<td align="left"><p>App-V 5,0 Management Server offre funzionalità di gestione complessive per l'infrastruttura App-V 5,0. Inoltre, è possibile installare più di un'istanza del server di gestione nell'ambiente che offre i vantaggi seguenti:</p>
<ul>
<li><p>Tolleranza di errore e disponibilità elevata: l'installazione e la configurazione del server di gestione App-V 5,0 in due computer distinti possono essere utili in situazioni in cui uno dei server non è disponibile o offline.</p>
<p>Puoi anche migliorare la disponibilità di App-V 5,0 installando il server di gestione in più computer. In questo scenario dovrebbe essere considerato anche un bilanciamento del carico di rete in modo che le richieste del server siano bilanciate.</p></li>
<li><p>Scalabilità: è possibile aggiungere altri server di gestione, se necessario, per supportare un carico elevato, ad esempio è possibile installare più server dietro un servizio di bilanciamento del carico.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0 Publishing Server</p></td>
<td align="left"><p>Il server di pubblicazione App-V 5,0 offre funzionalità per l'hosting e lo streaming di applicazioni virtuali. Il server di pubblicazione non richiede una connessione di database e supporta i protocolli seguenti:</p>
<ul>
<li><p>HTTP e HTTPS</p></li>
</ul>
<p>Puoi anche migliorare la disponibilità di App-V 5,0 installando il server di pubblicazione in più computer. Un sistema di bilanciamento del carico di rete deve essere considerato anche in modo che le richieste del server siano bilanciate.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 5,0 Reporting Server</p></td>
<td align="left"><p>Il server di report App-V 5,0 consente agli utenti autorizzati di eseguire e visualizzare report di App-V 5,0 esistenti e report ad hoc che consentono di gestire l'infrastruttura di App-V 5,0. Il server di Reporting richiede una connessione al database di report App-V 5,0. Puoi anche migliorare la disponibilità di App-V 5,0 installando il server di report in più computer. Un sistema di bilanciamento del carico di rete deve essere considerato anche in modo che le richieste del server siano bilanciate.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client App-V 5,0</p></td>
<td align="left"><p>Il client App-V 5,0 consente di eseguire i pacchetti creati con App-V 5,0 per l'esecuzione nei computer di destinazione.</p></td>
</tr>
</tbody>
</table>

 

**Nota**  Se si usa App-V 5,0 con Electronic Software Distribution (ESD), non è necessario usare il server di gestione di App-V 5,0, ma è comunque possibile utilizzare le funzionalità di creazione di report e flussi di App-V 5,0.

 






## Argomenti correlati


[Attività iniziali di App-V 5.0](getting-started-with-app-v-50--rtm.md)

 

 





