---
title: Eventi di attivazione di sincronizzazione per UE-V 2.x
description: Eventi di attivazione di sincronizzazione per UE-V 2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826796"
---
# Eventi di attivazione di sincronizzazione per UE-V 2.x


Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 consente di sincronizzare l'applicazione e le impostazioni di Windows in tutti i dispositivi collegati al dominio. *Gli eventi trigger di sincronizzazione* definiscono quando l'agente UE-V sincronizza queste impostazioni con il percorso di archiviazione delle impostazioni. UE-V 2 introduce un nuovo *metodo di sincronizzazione* denominato *SyncProvider*. Per altre informazioni sulla configurazione del metodo di sincronizzazione, vedere [metodi di sincronizzazione per UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).

## Eventi trigger di sincronizzazione di UE-V 2


La tabella seguente illustra gli eventi trigger per le applicazioni classiche e le impostazioni di Windows.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Evento trigger UE-V 2</strong></p></td>
<td align="left"><p><strong>SyncMethod = SyncProvider</strong></p></td>
<td align="left"><p><strong>SyncMethod = None</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Accesso di Windows</strong></p></td>
<td align="left"><ul>
<li><p>Le impostazioni dell'applicazione e di Windows vengono importate nella cache locale dalla posizione di archiviazione delle impostazioni.</p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)">Vengono applicate le impostazioni di Windows asincrone </a> .</p></li>
<li><p>Le impostazioni di Windows sincrone verranno applicate durante il successivo accesso di Windows.</p></li>
<li><p>Le impostazioni dell'applicazione verranno applicate all'avvio dell'applicazione.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Le impostazioni dell'applicazione e di Windows vengono lette direttamente dal percorso di archiviazione delle impostazioni.</p></li>
<li><p>Vengono applicate le impostazioni di Windows asincrone e sincrone.</p></li>
<li><p>Le impostazioni dell'applicazione verranno applicate all'avvio dell'applicazione.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Fine sessione di Windows</strong></p></td>
<td align="left"><p>Archiviare le modifiche localmente e memorizzare nella cache e copiare le impostazioni di Windows asincrone e sincrone nel server della posizione di archiviazione delle impostazioni, se disponibile</p></td>
<td align="left"><p>Archiviare le modifiche nel percorso di archiviazione delle impostazioni di Windows asincrono e sincrono</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows Connect (RDP)/Sblocca</strong></p></td>
<td align="left"><p>Sincronizza le impostazioni di Windows asincrone dalla posizione di archiviazione delle impostazioni alla cache locale, se disponibile.</p>
<p>Applicare le impostazioni di Windows memorizzate nella cache</p></td>
<td align="left"><p>Scaricare e applicare le impostazioni di Windows asincrone dalla posizione di archiviazione delle impostazioni</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows Disconnect (RDP)/Lock</strong></p></td>
<td align="left"><p>Archiviare le modifiche delle impostazioni di Windows asincrone nella cache locale.</p>
<p>Sincronizzare eventuali impostazioni di Windows asincrone dalla cache locale alla posizione di archiviazione delle impostazioni, se disponibile</p></td>
<td align="left"><p>Archiviare le impostazioni di Windows asincrone nella posizione di archiviazione delle impostazioni</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Inizio applicazione</strong></p></td>
<td align="left"><p>Applicare le impostazioni dell'applicazione dalla cache locale durante l'avvio dell'applicazione</p></td>
<td align="left"><p>Applicare le impostazioni dell'applicazione dalla posizione di archiviazione delle impostazioni durante l'avvio dell'applicazione</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Applicazione chiusa</strong></p></td>
<td align="left"><p>Archiviare eventuali modifiche delle impostazioni dell'applicazione nella cache locale e copiare le impostazioni nella posizione di archiviazione delle impostazioni, se disponibile</p></td>
<td align="left"><p>Archiviare le modifiche delle impostazioni dell'applicazione nella posizione di archiviazione delle impostazioni</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>L'attività pianificata del controller di sincronizzazione o "Sincronizza ora" viene eseguita dal centro impostazioni società</strong></p>
<p></p></td>
<td align="left"><p>Le impostazioni dell'applicazione e di Windows vengono sincronizzate tra la posizione di archiviazione delle impostazioni e la cache locale.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Le modifiche alle impostazioni non vengono memorizzate nella cache locale finché non viene chiusa un'applicazione. Questo trigger non esporterà le modifiche apportate a un'applicazione attualmente in uso.</p>
<p>Per le impostazioni di Windows, ciò significa che le eventuali modifiche non verranno memorizzate nella cache localmente ed esportate fino al blocco successivo (asincrono) o alla disconnessione (asincrono e sincrono).</p>
</div>
<div>

</div>
<p>Le impostazioni vengono applicate in questi casi:</p>
<ul>
<li><p>Le impostazioni di Windows asincrone vengono applicate direttamente.</p></li>
<li><p>Le impostazioni dell'applicazione vengono applicate all'avvio dell'applicazione.</p></li>
<li><p>Le impostazioni di Windows asincrone e sincrone vengono applicate durante l'accesso successivo di Windows.</p></li>
<li><p>Le impostazioni dell'app Windows (AppX) vengono applicate durante l'aggiornamento successivo. <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Per altre informazioni, vedere monitorare le impostazioni dell'applicazione </a> .</p></li>
</ul></td>
<td align="left"><p>N/D</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Impostazioni asincrone aggiornate in un archivio remoto *</strong></p></td>
<td align="left"><p>Caricare e applicare nuove impostazioni asincrone dalla cache.</p></td>
<td align="left"><p>Caricare e applicare le impostazioni da server centrale</p></td>
</tr>
</tbody>
</table>








## Argomenti correlati


[Documentazione tecnica su UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

[Modifica della frequenza delle attività pianificate di UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[Scegliere il metodo di configurazione per UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#config)









