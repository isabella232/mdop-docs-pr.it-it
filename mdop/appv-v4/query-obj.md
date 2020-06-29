---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815736"
---
# QUERY OBJ


Restituisce un elenco delimitato da tabulazioni di applicazioni correnti, pacchetti, associazioni di tipi di file o server di pubblicazione.

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

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
<td align="left"><p>APP</p></td>
<td align="left"><p>Restituisce un elenco di applicazioni.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PACCHETTO</p></td>
<td align="left"><p>Restituisce un elenco di pacchetti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TYPE</p></td>
<td align="left"><p>Restituisce un elenco di associazioni di tipi di file.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVER</p></td>
<td align="left"><p>Restituisce un elenco di server di pubblicazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/SHORT</p></td>
<td align="left"><p>Senza visualizzare le proprietà complete di ognuna, restituisce un elenco di nomi di applicazioni, pacchetti, associazioni o nomi di server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Per le applicazioni, restituisce tutte le applicazioni note anziché solo quelle a cui l'utente corrente ha accesso. Per i pacchetti, restituisce tutti i pacchetti noti anziché solo quelli a cui l'utente corrente ha accesso. Per le associazioni, restituisce solo le associazioni che si applicano a tutti gli utenti, non quelli specifici dell'utente. Non valido per i server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Se specificato, l'output viene registrato nel nome del percorso specificato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</p></td>
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

 

**Nota**  Nella versione 4,6 è stata aggiunta una nuova colonna all'output della QUERY SFTMIME OBJ: APP \ [/GLOBAL\]. L'ultima colonna dell'output è un valore numerico che indica se un'applicazione viene pubblicata o meno.

PUBLISHED = 1 indica che l'applicazione è stata pubblicata da un aggiornamento del server di pubblicazione, installando l'applicazione usando un file di Windows Installer (. MSI) oppure eseguendo un pacchetto di aggiunta di SFTMIME, configura il comando pacchetto o pubblica pacchetto usando un manifesto del pacchetto.

PUBLISHED = 0 indica che l'applicazione non è stata pubblicata o non è più pubblicata come risultato dell'esecuzione di un'operazione Clear o dell'esecuzione di un comando SFTMIME UNPUBLISH.

Se si usa il parametro/GLOBAL, lo stato pubblicato sarà 1 per le applicazioni pubblicate globalmente e 0 per le applicazioni pubblicate in contesti utente. Senza il parametro/GLOBAL, viene restituito uno stato pubblicato di 1 per le applicazioni pubblicate nel contesto dell'utente che esegue il comando e viene restituito uno stato di 0 per le applicazioni pubblicate globalmente.

 

Il comando SFTMIME QUERY OBJ può essere usato per richiedere informazioni su tutti gli oggetti visualizzati sopra: applicazioni, pacchetti, associazioni di tipi di file e server.Per mostrare come usare il comando SFTMIME QUERY OBJ nelle normali attività operative, nell'esempio seguente viene illustrato il processo da seguire se si vuole impostare il valore del parametro OVERRIDEURL per un pacchetto specifico per specificare un nuovo percorso per il contenuto del pacchetto. 

1.  Per trovare il pacchetto che si vuole configurare, eseguire il comando seguente:

    `SFTMIME QUERY OBJ:PACKAGE`

    Questo comando restituisce ogni nome di pacchetto individuato come GUID nella prima colonna di output, ad esempio {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.

2.  Per impostare il valore del parametro OVERRIDEURL, è possibile usare il comando [Configura pacchetto](configure-package.md) di SFTMIME. Ad esempio, per impostare il valore di OVERRIDEURL per il pacchetto su un valore di *\\\\server\\share\\mypackage.SFT*, usa il comando SFTMIME Configura pacchetto e assegnagli il GUID del pacchetto selezionato dall'output del comando SFTMIME query obj nel passaggio 1, seguito dal parametro OVERRIDEURL e dal relativo nuovo valore, come indicato di seguito:

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

Per la versione 4.6 SP2 è stata aggiunta l'opzione seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/NO-UPDATE-FTA-SHORTCUT</p></td>
<td align="left"><p>Indica lo stato corrente del flag/NO-UPDATE-FTA-SHORTCUT.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)

 

 





