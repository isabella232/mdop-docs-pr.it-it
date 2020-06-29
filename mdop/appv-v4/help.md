---
title: HELP
description: HELP
author: dansimp
ms.assetid: 0ddb5f18-0c0a-45ea-b7c7-2d4749e3d35d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 395e6199529ccbe708aa7d1ac6673ea6f9494ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821465"
---
# HELP


Visualizza le informazioni sui vari comandi di SFTMIME che possono essere usati in Application Virtualization (App-V).

## HELP


`SFTMIME [/? | /HELP [VERB:<verb>]]`

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
<td align="left"><p>/?,/HELP</p></td>
<td align="left"><p>Visualizza le informazioni sull'utilizzo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>verbo</p></td>
<td align="left"><p>Comando da eseguire, ad esempio Aggiungi, Aggiorna, guida o Rimuovi.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>oggetto</p></td>
<td align="left"><p>Il comando si applica a, ad esempio APP: &quot; applicazione predefinita.&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>parametri</p></td>
<td align="left"><p>Parametri facoltativi per il verbo e l'oggetto specificati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Registrare l'output nel nome del percorso specificato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Visualizza l'output nella finestra della console attiva (impostazione predefinita).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Visualizza gli errori in una finestra di dialogo (non valido per le query).</p></td>
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

 

Sono supportati i verbi descritti nella tabella seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>ADD</p></td>
<td align="left"><p>Aggiunge una nuova applicazione, un pacchetto, un'associazione di tipi di file o un server di pubblicazione al client App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CONFIGURARE</p></td>
<td align="left"><p>Modifica la configurazione di un'applicazione, di un pacchetto, di un'associazione di tipi di file o di un server di pubblicazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DELETE</p></td>
<td align="left"><p>Rimuove le applicazioni, i pacchetti, le associazioni di tipi di file o i server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CARICARE</p></td>
<td align="left"><p>Carica un pacchetto nella cache del file System.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RIPRISTINARE</p></td>
<td align="left"><p>Reimposta le impostazioni personali per un'applicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REFRESH</p></td>
<td align="left"><p>Attiva un aggiornamento del server di pubblicazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PUBBLICARE</p></td>
<td align="left"><p>Pubblica un collegamento a un'applicazione nel menu Start, nel desktop o in un'altra posizione specificata dell'utente o può essere usato per pubblicare il contenuto di un intero pacchetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ANNULLARE la pubblicazione</p></td>
<td align="left"><p>Rimuove i tasti di scelta rapida e i tipi di file per un intero pacchetto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>QUERY</p></td>
<td align="left"><p>Ottiene un elenco corrente di applicazioni, pacchetti, associazioni di tipi di file o server di pubblicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CHIARO</p></td>
<td align="left"><p>Rimuove le impostazioni personali e le configurazioni desktop per una o più applicazioni.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SCARICARE</p></td>
<td align="left"><p>Scarica un pacchetto dalla cache del file System.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BLOCCARE</p></td>
<td align="left"><p>Blocca l'applicazione specificata nella cache del file System.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SBLOCCARE</p></td>
<td align="left"><p>Sblocca l'applicazione specificata nella cache del file System.</p></td>
</tr>
</tbody>
</table>

 

Per altre informazioni sulle azioni precedenti, usare il comando seguente:

`SFTMIME /HELP VERB:verb`

Ad esempio, il comando seguente visualizzerà le informazioni per il verbo di aggiunta:

`SFTMIME /HELP VERB:ADD`

## Argomenti correlati


[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)

 

 





