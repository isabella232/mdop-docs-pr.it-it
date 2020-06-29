---
title: Finestra Cronologia
description: Finestra Cronologia
author: dansimp
ms.assetid: f11f9ad9-bffe-4c56-8c46-fe9c0a8e55c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02b4336409f33d6c1f2868bceb22cb95120f2198
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820786"
---
# Finestra Cronologia


La cronologia di un oggetto Criteri di gruppo può essere visualizzata facendo doppio clic su un GPO oppure facendo clic con il pulsante destro del mouse su un GPO e quindi scegliendo **cronologia**. Viene visualizzata anche nella console di **gestione di criteri di gruppo** come scheda per ogni oggetto.

La cronologia contiene un elenco di tutte le versioni dell'oggetto Criteri di stato selezionato salvate nell'archivio. Nella finestra **cronologia** è possibile ottenere un report delle impostazioni in un oggetto Criteri di gruppo, confrontare più versioni di un oggetto Criteri di gruppo o eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo.

## Filtrare gli eventi nella finestra cronologia


Le schede nella finestra **cronologia** filtrano gli eventi visualizzati.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schede</th>
<th align="left">Filtro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Mostra tutto</strong></p></td>
<td align="left"><p>Visualizza tutte le versioni del GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Archiviato</strong></p></td>
<td align="left"><p>Visualizza solo le versioni archiviate dell'oggetto Criteri di controllo. La versione distribuita viene omessa da questo elenco.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Solo etichette</strong></p></td>
<td align="left"><p>Visualizzare solo i GPO a cui sono associate etichette.</p></td>
</tr>
</tbody>
</table>

 

## Informazioni sugli eventi


Le informazioni vengono fornite per ogni evento nella cronologia del GPO selezionato.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Caratteristica GPO</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Computer</strong></p></td>
<td align="left"><p>Versione generata automaticamente della parte di configurazione del computer dell'oggetto Criteri di controllo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Utente</strong></p></td>
<td align="left"><p>Versione generata automaticamente della parte di configurazione utente dell'oggetto Criteri di controllo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Tempo</strong></p></td>
<td align="left"><p>Timestamp della versione del GPO quando è stata eseguita l'azione nel campo stato.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Stato</strong></p></td>
<td align="left"><p>Stato della versione selezionata del GPO:</p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong>Distribuito </strong> : questa versione dell'oggetto Criteri di controllo è attualmente attiva nell'ambiente di produzione.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Check-in </strong> : questa versione dell'oggetto Criteri di gruppo è disponibile per gli editori autorizzati per l'estrazione per la modifica o per l'amministratore dei criteri di raggruppamento da distribuire.</p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong>Estratto </strong> : questa versione dell'oggetto Criteri di controllo è attualmente estratta da un editor e non è disponibile per altri editor. Lo stato estratto non viene registrato nella <strong> pagina Cronologia </strong> tranne che per indicare se un oggetto Criteri di controllo è attualmente estratto.</p>
<p><img src="images/327623bd-0842-4372-be1f-bdc4b8c3481c.gif" alt="Created GPO icon" /> <strong>Created </strong> : identifica la data e l'ora della creazione iniziale del GPO.</p>
<p><img src="images/8356fcdc-1279-425b-ab14-a23bcfe391da.gif" alt="Labeled GPO icon" /> <strong>Etichettato </strong> : identifica una versione con etichetta dell'oggetto Criteri di controllo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Stato GPO</strong></p></td>
<td align="left"><p>La configurazione del computer e la configurazione dell'utente possono essere gestite separatamente. Questo stato Mostra le parti del GPO abilitate.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Proprietario</strong></p></td>
<td align="left"><p>La persona che ha eseguito l'accesso o ha distribuito l'oggetto Criteri di controllo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Comment</strong></p></td>
<td align="left"><p>Un commento immesso dal proprietario di un oggetto Criteri di controllo al momento della modifica di questa versione. Utile per identificare le specifiche della versione in caso di necessità di eseguire il rollback a una versione precedente.</p></td>
</tr>
</tbody>
</table>

 

## Rapporti


A seconda che sia selezionata una singola versione di GPO o più versioni di GPO, i pulsanti **Impostazioni** e **differenze** visualizzano i report sulle impostazioni degli oggetti Criteri di gruppo. Facendo clic con il pulsante destro del mouse su versioni GPO è disponibile l'opzione per visualizzare anche i report basati su XML.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Button</th>
<th align="left">Effetto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Impostazioni</strong></p></td>
<td align="left"><p>Generare un report basato su HTML che visualizzi le impostazioni nella versione selezionata del GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Differenze</strong></p></td>
<td align="left"><p>Generare un report basato su HTML che confronti le impostazioni in più versioni selezionate dell'oggetto Criteri di gruppo.</p></td>
</tr>
</tbody>
</table>

 

### Chiave per i report differenze

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Simbolo</th>
<th align="left">Significato</th>
<th align="left">Colore</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>L'elemento esiste con impostazioni identiche in entrambi i GPO</p></td>
<td align="left"><p>Varia in base al livello</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[#]</strong></p></td>
<td align="left"><p>L'elemento è presente in entrambi i GPO, ma con le impostazioni modificate</p></td>
<td align="left"><p>Blu</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>[-]</strong></p></td>
<td align="left"><p>L'elemento esiste solo nel primo GPO</p></td>
<td align="left"><p>Rosso</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[+]</strong></p></td>
<td align="left"><p>L'elemento esiste solo nel secondo GPO</p></td>
<td align="left"><p>Verde</p></td>
</tr>
</tbody>
</table>

 

-   Per gli elementi con impostazioni modificate, le impostazioni modificate vengono identificate quando l'elemento viene espanso. Il valore dell'attributo in ogni oggetto Criteri di ricerca viene visualizzato nello stesso ordine in cui vengono visualizzati i GPO nel report.

-   Alcune modifiche alle impostazioni possono comportare la segnalazione di un elemento come due elementi diversi (uno presente solo nel primo GPO, uno presente solo nel secondo), anziché un elemento modificato.

### Riferimenti aggiuntivi

-   [Scheda Contenuto](contents-tab.md)

 

 





