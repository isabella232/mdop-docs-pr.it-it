---
title: PUBLISH PACKAGE
description: PUBLISH PACKAGE
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815815"
---
# PUBLISH PACKAGE


Pubblica il contenuto di un intero pacchetto.

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Nome utente-visibile e user-friendly per il pacchetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Percorso manifesto/manifest&gt;</p></td>
<td align="left"><p>Il percorso o l'URL del file manifesto che elenca le applicazioni incluse nel pacchetto e tutte le relative informazioni di pubblicazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Se presente, il pacchetto sarà disponibile per tutti gli utenti di questo computer.</p></td>
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

 

**Importante**  Il pacchetto deve essere già stato aggiunto al client Application Virtualization e il file manifesto è obbligatorio.

Per usare il parametro **Global** , il comando pubblica pacchetto deve essere eseguito come amministratore locale. in caso contrario, sono necessarie solo le autorizzazioni **ManageTypes** e **PublishShortcut** .

La pubblicazione senza il parametro **globale** concede all'utente l'accesso alle applicazioni nel pacchetto e pubblica i tipi di file e i tasti di scelta rapida elencati nel manifesto nel profilo dell'utente.

La pubblicazione con il parametro **Global** aggiunge i tipi di file e i tasti di scelta rapida elencati nel manifesto al profilo "tutti gli utenti".

Se il pacchetto non è globale prima della chiamata e viene usato il parametro **globale** , il pacchetto viene reso globale e disponibile per tutti gli utenti.

 

## Argomenti correlati


[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)

 

 





