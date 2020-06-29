---
title: UNLOAD PACKAGE
description: UNLOAD PACKAGE
author: dansimp
ms.assetid: a076eb5a-ce3d-49e4-ac7a-4d4df10e3477
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fbee040f97bf5675ace7e873741a4270a993a911
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815146"
---
# UNLOAD PACKAGE


Scarica il pacchetto dalla cache del file System.

`SFTMIME UNLOAD PACKAGE:package-name [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Nome del pacchetto da scaricare.</p></td>
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

 

 





