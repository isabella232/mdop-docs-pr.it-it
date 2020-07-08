---
title: Elenco di controllo installazione di App-V
description: Elenco di controllo installazione di App-V
author: dansimp
ms.assetid: b17efaab-cd6d-4c30-beb7-c6e7c9c87657
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d6d83ac465a7e48dd35bd2fe966c3c51be24c96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819815"
---
# Elenco di controllo installazione di App-V


L'elenco di controllo seguente ha lo scopo di specificare una lista di elementi di alto livello da considerare e delineare i passaggi da eseguire per installare i server di Microsoft Application Virtualization (App-V).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Riferimento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Installare App-V Management Server. Se si sta installando il servizio Web di gestione, la console di gestione o l'archivio dati in server diversi, è possibile usare l'opzione di installazione personalizzata.</p></td>
<td align="left"><p><a href="how-to-install-application-virtualization-management-server.md" data-raw-source="[How to Install Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)">Come installare il server di gestione di Application Virtualization</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Installare il servizio Web di gestione App-V. (Facoltativo ¹)</p></td>
<td align="left"><p><a href="how-to-install-the-management-web-service.md" data-raw-source="[How to Install the Management Web Service](how-to-install-the-management-web-service.md)">Come installare il servizio Gestione Web</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installare la console di gestione di App-V. (Facoltativo ¹)</p></td>
<td align="left"><p><a href="how-to-install-the-management-console.md" data-raw-source="[How to Install the Management Console](how-to-install-the-management-console.md)">Come installare la console di gestione</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Installare l'App-V Data Store. (Facoltativo ¹)</p></td>
<td align="left"><p><a href="how-to-install-a-database.md" data-raw-source="[How to Install a Database](how-to-install-a-database.md)">Come installare un database</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installare il client App-V.</p></td>
<td align="left"><p><a href="how-to-manually-install-the-application-virtualization-client.md" data-raw-source="[How to Manually Install the Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)">Come installare manualmente Application Virtualization Client</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Installare App-V Sequencer.</p></td>
<td align="left"><p><a href="how-to-install-the-application-virtualization-sequencer.md" data-raw-source="[How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)">Come installare Application Virtualization Sequencer</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installare App-V Streaming Server. (Facoltativo e obbligatorio solo se si sta installando il server di streaming).</p></td>
<td align="left"><p><a href="how-to-install-the-application-virtualization-streaming-server.md" data-raw-source="[How to Install the Application Virtualization Streaming Server](how-to-install-the-application-virtualization-streaming-server.md)">Come installare Application Virtualization Streaming Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Creare directory di contenuto nei server che verranno usati per lo streaming delle applicazioni nei computer degli utenti.</p></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Come configurare i server di gestione di Application Virtualization</a></p>
<p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)">Come configurare Application Virtualization Streaming Server</a></p>
<p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)">Come configurare il server per IIS</a></p>
<p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)">Come configurare il file server</a></p></td>
</tr>
</tbody>
</table>

 

¹ questo è necessario solo se si sta installando il servizio Web di gestione App-V, la console di gestione o l'archivio dati in un altro computer.

## Argomenti correlati


[Elenchi di controllo per la distribuzione e l'aggiornamento di Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

[Elenco di controllo post-installazione di App-V](app-v-postinstallation-checklist.md)

 

 





