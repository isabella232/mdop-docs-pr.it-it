---
title: Funzionalità comuni della scheda Secondario
description: Funzionalità comuni della scheda Secondario
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819086"
---
# Funzionalità comuni della scheda Secondario


Ogni scheda secondaria include due sezioni, ovvero**oggetti Criteri di gruppo** e **gruppi e utenti**.

## Sezione oggetti Criteri di gruppo


La sezione **oggetti Criteri di gruppo** consente di visualizzare un elenco filtrato degli oggetti Criteri di gruppo e di identificare le caratteristiche seguenti per ogni GPO:

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
<td align="left"><p><strong>Name</strong></p></td>
<td align="left"><p>Nome dell'oggetto Criteri di gruppo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Computer (comp.)</strong></p></td>
<td align="left"><p>Versione generata automaticamente della parte di configurazione del computer dell'oggetto Criteri di controllo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Utente</strong></p></td>
<td align="left"><p>Versione generata automaticamente della parte di configurazione utente dell'oggetto Criteri di controllo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Stato</strong></p></td>
<td align="left"><p>Stato dell'oggetto Criteri di selezione selezionato:</p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong>Non controllata: </strong> non gestita da Advanced Group Policy Management.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Archiviato: </strong> disponibile per gli editor autorizzati per l'estrazione per la modifica o per un amministratore di criteri di gruppo da distribuire.</p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong>Estratto: </strong> attualmente in fase di modifica. Non è disponibile per altri editor per l'estrazione fino a quando l'editor non l'ha estratto o un amministratore della gestione avanzata Criteri di controllo.</p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong>In sospeso: in attesa </strong> di approvazione da un amministratore di criteri di gruppo prima di essere creato, controllato, distribuito o eliminato.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Eliminata: </strong> eliminata dall'archivio, ma comunque in grado di essere ripristinata.</p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong>Modello: </strong> versione statica di un oggetto Criteri di ricerca da usare come punto di partenza per la creazione di nuovi GPO.</p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong>Modello (impostazione predefinita): </strong> per impostazione predefinita, questo modello rappresenta il punto di partenza usato per la creazione di un nuovo oggetto Criteri di stato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Stato GPO</strong></p></td>
<td align="left"><p>La configurazione del computer e la configurazione dell'utente possono essere gestite separatamente. Lo stato dell'oggetto Criteri di stato indica quali parti del GPO sono abilitate.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Filtro WMI</strong></p></td>
<td align="left"><p>Visualizzare i filtri WMI applicati a questo oggetto Criteri di stato. I filtri WMI vengono gestiti nel <strong> nodo filtri WMI </strong> per il dominio nell'albero della console di GPMC.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modificato</strong></p></td>
<td align="left"><p>Per un GPO controllato, la data più recente in cui è stata archiviata dopo essere stata modificata o disattivata per la modifica. Per un GPO non controllato, la data in cui è stata modificata l'ultima volta.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Proprietario</strong></p></td>
<td align="left"><p>L'editor che ha effettuato l'accesso o l'approvatore che ha distribuito l'oggetto Criteri di selezione selezionato.</p></td>
</tr>
</tbody>
</table>

 

## Sezione gruppi e utenti


Quando viene selezionato un oggetto Criteri di gruppo, nella sezione **gruppi e utenti** viene visualizzato un elenco di gruppi e utenti con accesso a tale oggetto Criteri di gruppo. Le autorizzazioni e l'ereditarietà consentite vengono visualizzate per ogni gruppo o utente. Un amministratore della gestione avanzata Criteri di amministrazione può configurare le autorizzazioni usando ruoli Advanced Group Policy Management (editor, approvatore e revisore) o una combinazione personalizzata di autorizzazioni.

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

-   Per informazioni su ruoli e autorizzazioni correlati a specifiche attività, vedere le attività in [esecuzione di attività di amministratore della gestione avanzata Criteri di amministrazione](performing-agpm-administrator-tasks.md), esecuzione di attività dell' [Editor](performing-editor-tasks.md), esecuzione di [attività di approvazione](performing-approver-tasks.md)ed esecuzione di [attività del revisore](performing-reviewer-tasks.md).

### Riferimenti aggiuntivi

-   [Scheda Contenuto](contents-tab.md)

 

 





