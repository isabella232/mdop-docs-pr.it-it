---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822396"
---
# ADD PACKAGE


Aggiunge un record del pacchetto. Se il pacchetto esiste già, questo comando aggiornerà la configurazione del pacchetto esistente.

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Percorso del file manifesto che elenca le applicazioni incluse nel pacchetto e tutte le relative informazioni di pubblicazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;URL/OVERRIDEURL&gt;</p></td>
<td align="left"><p>Posizione del file SFT del pacchetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>Il caricamento in background viene eseguito dopo un aggiornamento della pubblicazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>Il caricamento in background viene eseguito quando un utente effettua l'accesso.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>Il caricamento in background viene eseguito dopo che un utente avvia un'applicazione dal pacchetto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Destinazione/AUTOLOADTARGET</p></td>
<td align="left"><p>Indica quali applicazioni del pacchetto verranno caricate di carico.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NESSUNO</p></td>
<td align="left"><p>Non verrà eseguito alcun caricamento del carico, nonostante la presenza di eventuali flag/AUTOLOADONxxx.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TUTTI</p></td>
<td align="left"><p>Se è abilitato un trigger di autoload, tutte le applicazioni nel pacchetto verranno caricate nella cache indipendentemente dal fatto che siano o meno già avviate.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Se è abilitato un trigger di autoload, il pacchetto verrà caricato se le applicazioni di questo pacchetto sono state avviate in precedenza da un utente.</p></td>
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

 

## Argomenti correlati


[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)

 

 





