---
title: Funzionalità della scheda Contenuto
description: Funzionalità della scheda Contenuto
author: dansimp
ms.assetid: f1f4849d-bf94-47d5-ad81-0eee33abcaca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 081cffb7c2871d0e49abd229ec06773726483f2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818895"
---
# Funzionalità della scheda Contenuto


Ogni scheda secondaria nella scheda **Sommario** include due sezioni, ovvero**oggetti Criteri di gruppo** e **gruppi e utenti**.

## Sezione oggetti Criteri di gruppo


Nella sezione **oggetti Criteri di gruppo** viene visualizzato un elenco filtrato degli oggetti Criteri di gruppo e vengono identificati gli attributi seguenti per ogni GPO. È possibile usare la casella di **ricerca** per cercare GPO con attributi specifici. Per altre informazioni, vedere [cercare e filtrare l'elenco degli oggetti Criteri di ricerca](search-and-filter-the-list-of-gpos.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attributo GPO</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Name</strong></p></td>
<td align="left"><p>Nome dell'oggetto Criteri di stato.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Stato</strong></p></td>
<td align="left"><p>Stato dell'oggetto Criteri di stato selezionato</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modificato da</strong></p></td>
<td align="left"><p>L'editor che ha effettuato l'accesso o l'approvatore che ha distribuito l'oggetto Criteri di selezione selezionato.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Modifica data</strong></p></td>
<td align="left"><p>Per un GPO controllato, la data più recente in cui è stata archiviata dopo essere stata modificata o disattivata per la modifica. Per un GPO non controllato, la data in cui è stata modificata l'ultima volta.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Comment</strong></p></td>
<td align="left"><p>Un commento immesso dalla persona che ha effettuato l'accesso o ha distribuito un oggetto Criteri di controllo nel momento in cui è stato modificato. Utile per identificare le specifiche della versione in caso di necessità di eseguire il rollback a una versione precedente.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Versione computer</strong></p></td>
<td align="left"><p>Versione generata automaticamente della parte di configurazione del computer del GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Versione utente</strong></p></td>
<td align="left"><p>Versione generata automaticamente della parte di configurazione dell'utente dell'oggetto Criteri di controllo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Stato GPO</strong></p></td>
<td align="left"><p>La configurazione del computer e la configurazione dell'utente possono essere gestite separatamente. Lo stato dell'oggetto Criteri di stato indica quali parti del GPO sono abilitate.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Filtro WMI</strong></p></td>
<td align="left"><p>Visualizzare i filtri WMI applicati a questo oggetto Criteri di stato. I filtri WMI vengono gestiti nella <strong> cartella filtri WMI </strong> per il dominio nell'albero della console di GPMC.</p></td>
</tr>
</tbody>
</table>

 

## Sezione gruppi e utenti


Quando viene selezionato un oggetto Criteri di gruppo, nella sezione **gruppi e utenti** viene visualizzato un elenco di gruppi e utenti con accesso a tale oggetto Criteri di gruppo. Le autorizzazioni e l'ereditarietà consentite vengono visualizzate per ogni gruppo o utente. Un amministratore della gestione avanzata Criteri di amministrazione può configurare le autorizzazioni usando ruoli Advanced Group Policy Management (editor, approvatore, revisore e amministratore della gestione avanzata) o una combinazione personalizzata di autorizzazioni.

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
<td align="left"><p><strong>Aggiungi</strong></p></td>
<td align="left"><p>Aggiungere una nuova voce al descrittore di sicurezza. È possibile aggiungere qualsiasi utente o gruppo in Active Directory.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Rimuovi</strong></p></td>
<td align="left"><p>Rimuovere la voce selezionata dall'elenco di controllo di Access.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Proprietà</strong></p></td>
<td align="left"><p>Visualizzare le proprietà per l'oggetto selezionato. La pagina delle proprietà è la stessa visualizzata per un oggetto in <strong> utenti e computer di Active Directory </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Avanzate</strong></p></td>
<td align="left"><p>Aprire l' <strong> Editor elenco di controllo di Access </strong> .</p></td>
</tr>
</tbody>
</table>

 

### Considerazioni aggiuntive

-   Per informazioni su ruoli e autorizzazioni correlati a specifiche attività, vedere le attività in [esecuzione di attività di amministratore della gestione avanzata Criteri di amministrazione](performing-agpm-administrator-tasks-agpm40.md), esecuzione di attività dell' [Editor](performing-editor-tasks-agpm40.md), esecuzione di [attività di approvazione](performing-approver-tasks-agpm40.md)ed esecuzione di [attività del revisore](performing-reviewer-tasks-agpm40.md).

### Riferimenti aggiuntivi

-   [Scheda Contenuto](contents-tab-agpm40.md)

 

 





