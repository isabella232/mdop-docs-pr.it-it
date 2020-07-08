---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822385"
---
# ADD TYPE


Aggiunge l'associazione di tipi di file specificata.

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>DIGITARE: &lt; File-Extension&gt;</p></td>
<td align="left"><p>Estensione del nome di file che verrà associata all'applicazione specificata.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Applicazione/App&gt;</p></td>
<td align="left"><p>Nome e versione (facoltativa) dell'applicazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Icona/icona-percorso&gt;</p></td>
<td align="left"><p>Il percorso o l'URL per il file dell'icona.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Tipo di/Description-DESC&gt;</p></td>
<td align="left"><p>Nome descrittivo dell'utente per il tipo di file. Impostazione predefinita per il &quot; file di estensione.&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Tipo di contenuto/Content-Type&gt;</p></td>
<td align="left"><p>Tipo di contenuto del file. Impostazione predefinita per &quot; application/softricity-extension.&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Se presente, il pacchetto sarà disponibile per tutti gli utenti di questo computer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Tipo di/perceived-Type percepito&gt;</p></td>
<td align="left"><p>Tipo di file percepito. Il valore predefinito è Nothing.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/PROGID &lt; ProgID&gt;</p></td>
<td align="left"><p>Identificatore a livello di codice per il tipo di file. Per impostazione predefinita, l'App Virt. Extension. file.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONFIRMOPEN</p></td>
<td align="left"><p>Indica se gli utenti che scaricano un file di questo tipo devono essere chiesti se aprire o salvare il file. Il valore predefinito è sì.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOWEXT</p></td>
<td align="left"><p>Indica se l'estensione del file deve essere sempre visualizzata, anche se l'utente ha richiesto che tutte le estensioni vengano nascoste. Il valore predefinito è NO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/NEWMENU</p></td>
<td align="left"><p>Indica se una voce deve essere aggiunta al <strong> nuovo menu della shell </strong> . Il valore predefinito è NO.</p></td>
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

 

 





