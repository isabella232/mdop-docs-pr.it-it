---
title: CONFIGURE SERVER
description: CONFIGURE SERVER
author: dansimp
ms.assetid: c916eddd-74f2-46e4-953d-120b23284e37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7757f281ec57645d20367056ba0013ef476a91a1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821975"
---
# CONFIGURE SERVER


Consente a un utente di modificare la configurazione di un server; le impostazioni non specificate non verranno modificate.

`SFTMIME CONFIGURE SERVER:server-name [/NAME display-name] [/HOST hostname]                 [/PORT port] [/PATH path] [/TYPE {HTTP|RTSP}]                 [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parametro</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SERVER: &lt; nome server&gt;</p></td>
<td align="left"><p>Nome visualizzato per il server di pubblicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/NAME &lt; -nome visualizzato&gt;</p></td>
<td align="left"><p>Nuovo nome visualizzato per il server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Hostname/host&gt;</p></td>
<td align="left"><p>Il nome host o l'indirizzo IP per il server di pubblicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Porta/Port&gt;</p></td>
<td align="left"><p>Porta in cui è in ascolto il server di pubblicazione. Il valore predefinito è 80 per i normali server HTTP, 443 per i server HTTP con sicurezza avanzata, 554 per i normali server di virtualizzazione delle applicazioni e 322 per i server che usano la sicurezza avanzata.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Percorso/path&gt;</p></td>
<td align="left"><p>Parte del percorso dell'URL usato in una richiesta di pubblicazione. Se il parametro TYPE è impostato su RTSP, il percorso è facoltativo e il valore predefinito è &quot; / &quot; .</p></td>
</tr>
<tr class="even">
<td align="left"><p>/TYPE</p></td>
<td align="left"><p>Indica se il server di pubblicazione è un server Web ( &quot; http &quot; ) o un Application Virtualization Server ( &quot; RTSP &quot; ).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/REFRESH</p></td>
<td align="left"><p>Se impostato su attivato, le informazioni di pubblicazione verranno aggiornate quando l'utente effettua l'accesso. Impostazioni predefinite su attivato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SECURE</p></td>
<td align="left"><p>Se presente, indica che nel server di pubblicazione deve essere stabilita una connessione con sicurezza avanzata.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Se specificato, l'output viene registrato nel nome del percorso specificato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</p></td>
</tr>
</tbody>
</table>

 

Per la versione 4.6 è stata aggiunta l'opzione seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/LOGU</p></td>
<td align="left"><p>Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)

 

 





