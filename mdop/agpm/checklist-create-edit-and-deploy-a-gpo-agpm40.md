---
title: Elenco di controllo per creare, modificare e distribuire un GPO
description: Elenco di controllo per creare, modificare e distribuire un GPO
author: dansimp
ms.assetid: 44631bed-16d2-4b5a-af70-17a73fb5f6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d8bea9109040aa81a20df62356ef1d307d5eac0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819105"
---
# Elenco di controllo: Creare, modificare e distribuire un oggetto Criteri di gruppo


In un ambiente in cui più persone modificano gli oggetti Criteri di gruppo tramite Advanced Group Policy Management (Advanced criteri di gruppo), un amministratore della gestione avanzata (controllo completo) delega l'autorizzazione per gli editor, i responsabili approvazione e i revisori sia come gruppi che come singoli. Di seguito è riportato un processo di sviluppo GPO tipico per un editor e un responsabile approvazione.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività</th>
<th align="left">Riferimento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Editor richiede la creazione di un nuovo oggetto Criteri di stato o un responsabile dell'approvazione crea un nuovo oggetto Criteri di stato.</p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)">Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato</a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)">Creare un nuovo oggetto Criteri di gruppo controllato</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>L'approvatore approva la creazione del GPO se richiesto da un editor.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Approvare o rifiutare un'azione in sospeso</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Editor estrae una copia del GPO dall'archivio in modo che nessun altro possa modificare l'oggetto Criteri di controllo. Editor apporta modifiche al GPO e quindi controlla l'oggetto Criteri di controllo modificato nell'archivio.</p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)">Modificare un oggetto Criteri di gruppo offline</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Se si sviluppa in una foresta di test, editor Esporta il GPO in un file, trasferisce il file nella foresta di produzione e importa il file. Inoltre, un editor può collegare l'oggetto Criteri di gruppo a un'unità organizzativa che contiene computer e utenti di test.</p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)">Uso di un ambiente di test</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Editor richiede la distribuzione del GPO nell'ambiente di produzione del dominio.</p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)">Richiedere la distribuzione di un oggetto Criteri di gruppo</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>I revisori, ad esempio i responsabili approvazione o gli editori, analizzano l'oggetto Criteri di tipo.</p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)">Attività del revisore</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>L'approvatore approva e distribuisce il GPO nell'ambiente di produzione del dominio o rifiuta il GPO.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Approvare o rifiutare un'azione in sospeso</a></p></td>
</tr>
</tbody>
</table>

 

### Riferimenti aggiuntivi

[Gestione avanzata Criteri di gruppo 4.0](advanced-group-policy-management-40.md)

 

 





