---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819346"
---
# CONFIGURE PACKAGE


Consente all'utente di modificare un file manifesto del pacchetto, un'origine pacchetto, tipi di trigger di caricamento o destinazione di caricamento per un pacchetto.

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

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
<td align="left"><p>&lt;URL/OVERRIDEURL&gt;</p></td>
<td align="left"><p>Posizione del file SFT del pacchetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADNEVER</p></td>
<td align="left"><p>Il caricamento in background è disattivato per il pacchetto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>Il caricamento in background viene eseguito dopo un aggiornamento della pubblicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>Il caricamento in background viene eseguito quando un utente effettua l'accesso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>Il caricamento in background viene eseguito dopo che un utente avvia un'applicazione dal pacchetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Destinazione/AUTOLOADTARGET&gt;</p></td>
<td align="left"><p>Indica quali applicazioni del pacchetto verranno caricate di carico.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NESSUNO</p></td>
<td align="left"><p>Non verranno eseguiti carichi di carica automatici, nonostante la presenza di eventuali flag/AUTOLOADONxxx.</p></td>
</tr>
<tr class="even">
<td align="left"><p>TUTTI</p></td>
<td align="left"><p>Se è abilitato un trigger di autoload, tutte le applicazioni nel pacchetto verranno caricate nella cache, indipendentemente dal fatto che siano state avviate.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Se è abilitato un trigger di autoload, il pacchetto verrà caricato se le applicazioni di questo pacchetto sono state avviate in precedenza da un utente.</p></td>
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

 

Per la versione 4.6 SP2 è stata aggiunta l'opzione seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>[/NO-UPDATE-FTA-SHORTCUT {TRUE | FALSE} {/GLOBAL}]</p></td>
<td align="left"><p>Se impostato su TRUE, viene creato un valore del registro di sistema per il pacchetto, per ogni utente o a livello globale, se è specificato il flag/GLOBAL.</p>
<p>Se impostato su FALSE, il valore del registro di sistema viene rimosso e le associazioni di tipi di file (FTA) per il pacchetto vengono reinstallate.</p>
<p>Se non specificato, si verifica un comportamento normale di FTA e di pubblicazione rapida. Se si eseguono le operazioni successive di aggiornamento delle pubblicazioni nel client App-V 4,6 SP2, le scelte rapide e accordi per i pacchetti che hanno questo set di valori del registro di sistema non verranno modificate e i tasti di scelta rapida e accordi non verranno registrati all'avvio o all'accesso dell'utente, a meno che non si reimposti il contrassegno.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Funziona in combinazione con il flag/NO-UPDATE-FTA-SHORTCUT. Se il contrassegno/GLOBAL è presente, indica che verrà creato un valore del registro di sistema per tutti gli utenti. Per impostazione predefinita, il valore del registro di sistema viene creato solo per l'utente.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)

 

 





