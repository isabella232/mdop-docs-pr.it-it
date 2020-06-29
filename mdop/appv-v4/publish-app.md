---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815816"
---
# PUBLISH APP


Pubblica un collegamento a un'applicazione nel menu Start dell'utente, nel desktop o in un'altra posizione specificata.

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>APPLICAZIONE: &lt; applicazione&gt;</p></td>
<td align="left"><p>Nome e versione (facoltativa) dell'applicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/DESKTOP</p></td>
<td align="left"><p>Pubblica un collegamento al desktop dell'utente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/START</p></td>
<td align="left"><p>Pubblica un collegamento alla cartella Application Virtualization Applications nella cartella Programs del menu Start.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/TARGET &lt; target-Path&gt;</p></td>
<td align="left"><p>Percorso assoluto in cui deve essere pubblicato il collegamento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Icona/icona-percorso&gt;</p></td>
<td align="left"><p>Il percorso o l'URL per il file dell'icona.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/DISPLAY &lt; -nome visualizzato&gt;</p></td>
<td align="left"><p>Nome visualizzato per il collegamento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Comando/args-args&gt;</p></td>
<td align="left"><p>Parametri da passare all'applicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Se specificato, l'output viene registrato nel nome del percorso specificato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</p></td>
</tr>
<tr class="even">
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

 

 





