---
title: LOAD PACKAGE
description: LOAD PACKAGE
author: dansimp
ms.assetid: eb19116d-e5d0-445c-b2f0-3116a09384d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 938aa92696c8530c91d9a7acaac42408de534edc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816236"
---
# LOAD PACKAGE


Carica il pacchetto specificato nella cache del file System.

`SFTMIME LOAD PACKAGE:package-name [/SFTPATH sft-pathname]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>PACCHETTO: &lt; nome pacchetto&gt;</p></td>
<td align="left"><p>Nome del pacchetto da caricare.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SFTPATH &lt; SFT-PathName&gt;</p></td>
<td align="left"><p>Se specificato, il percorso di un file SFT da cui caricare.</p></td>
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

 

**Nota**  Se non viene specificato alcun SFTPATH, il client caricherà il pacchetto utilizzando il percorso configurato per l'uso, in base al file OSD, al valore della chiave del registro di sistema ApplicationSourceRoot o all'impostazione di OverrideURL.

Il comando **Carica pacchetto** esegue un caricamento sincrono e non sarà completo finché il pacchetto non viene caricato completamente o finché non incontra una condizione di errore.

 

## Argomenti correlati


[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)

 

 





