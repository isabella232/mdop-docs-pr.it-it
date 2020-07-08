---
title: Come generare report
description: Come generare report
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826995"
---
# Come generare report


I tipi di report seguenti possono essere creati dagli amministratori in MED-V:

-   [Stato](#bkmk-generatingastatusreport): usa il rapporto sullo stato per esaminare lo stato corrente di tutti gli utenti attivi e tutte le aree di lavoro MED-V di ogni utente in base a un determinato periodo di tempo. Ciò include la visualizzazione di computer attualmente connessi al server o, se non sono attualmente connessi, la data e l'ora in cui sono stati connessi per ultimo al server, lo stato di ogni computer e altre informazioni rilevanti.

-   [Log attività](#bkmk-generatinganactivitylogreport): usare questo report per esaminare gli eventi originati da un utente o un host specifico in un intervallo di date definito.

-   [Log errori](#bkmk-generatinganerrorlogreport): usare questo report per visualizzare gli errori originati da un utente o un host specifico in un intervallo di date definito.

I risultati del report possono essere ordinati in base a qualsiasi colonna facendo clic sul nome della colonna appropriata.

I risultati del report possono essere raggruppati trascinando un'intestazione di colonna nella parte superiore del report. Trascinare più intestazioni di colonna per raggruppare una colonna dopo l'altra.

## <a href="" id="bkmk-generatingastatusreport"></a>Come generare un report sullo stato


**Per generare un report sullo stato**

1.  Fare clic sul pulsante Gestione **report** .

2.  Nel modulo **report** scegliere **stato**dal menu **tipi di report** e fare clic su **genera**.

    Verrà visualizzata la finestra di dialogo parametri rapporto.

3.  Nella finestra di dialogo **parametri rapporto** , nel campo **numero di giorni** , immettere un numero o usare le frecce per selezionare il numero di giorni da includere nel report di stato e fare clic su **OK**.

    Viene generato un report di stato. I parametri del report sono definiti nella tabella seguente.

**Proprietà area di lavoro client MED-V**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Proprietà</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tempo</p></td>
<td align="left"><p>Data e ora in cui si è verificato l'evento.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Per impostazione predefinita, gli eventi vengono visualizzati in ordine di data decrescente. Tuttavia, può essere modificato facendo clic sulla colonna data/ora ricevuta.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Nome utente</p></td>
<td align="left"><p>L'utente che ha avviato l'evento.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se l'evento si è verificato prima che un utente abbia effettuato l'accesso, il nome utente è SYSTEM.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome host</p></td>
<td align="left"><p>Il nome del computer host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome area di lavoro</p></td>
<td align="left"><p>Nome dell'area di lavoro MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome computer area di lavoro</p></td>
<td align="left"><p>Nome del computer in cui è in uso l'area di lavoro MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Online</p></td>
<td align="left"><p>Lo stato corrente del computer client:</p>
<ul>
<li><p><strong>Ha smesso</strong></p></li>
<li><p><strong>Iniziato alla &lt; data e ora in cui è stata avviata l'area di lavoro&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Versione client</p></td>
<td align="left"><p>Numero di versione del client.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versione dei criteri</p></td>
<td align="left"><p>La versione del criterio attualmente utilizzata dall'area di lavoro MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome immagine</p></td>
<td align="left"><p>Nome dell'immagine.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versione immagine</p></td>
<td align="left"><p>Versione dell'immagine che l'area di lavoro MED-V sta attualmente usando.</p>
<div class="alert">
<strong>Nota</strong><br/><p>La versione dell'area di lavoro MED-V può essere sconosciuta se non è stata ancora scaricata nel computer.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a>Come generare un report del log attività


**Per generare un report del log attività**

1.  Fare clic sul pulsante Gestione **report** .

    Viene visualizzato il modulo report.

2.  Nel modulo **report** selezionare **log attività**dal menu **tipi di report** e fare clic su **genera**.

3.  Nella finestra di dialogo **parametri report** configurare uno o più dei parametri seguenti:

    -   **Numero di giorni**: il numero di giorni da visualizzare nel report.

    -   **Nome utente contiene**: ogni evento in cui il nome utente contiene il testo immesso è incluso nel report.

    -   **Host Name Contains**: ogni evento in cui il nome host contiene il testo immesso è incluso nel report.

4.  Fai clic su **OK**.

    Viene generato un report con gli eventi e le date selezionati. I parametri del report sono definiti nella tabella seguente.

**Proprietà del report del log attività**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Proprietà</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ID evento</p></td>
<td align="left"><p>ID evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gravità</p></td>
<td align="left"><p><strong>Informazioni, errore, avviso</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Categoria</p></td>
<td align="left"><p>Il modulo a cui fa riferimento il report.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Descrizione dell'evento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tempo ricevuto</p></td>
<td align="left"><p>Data e ora in cui l'evento è stato ricevuto nel server.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se il client sta lavorando offline, il server riceve i report quando il client è online.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Nota</strong><br/><p>Per impostazione predefinita, gli eventi vengono visualizzati in ordine di data decrescente. Tuttavia, può essere modificato facendo clic sulla <strong> colonna data/ora ricevuta </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Ora client</p></td>
<td align="left"><p>La data e l'ora in cui si è verificato l'evento in base all'orologio client.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome host</p></td>
<td align="left"><p>Il nome del computer host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome utente</p></td>
<td align="left"><p>L'utente che ha avviato l'evento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome area di lavoro</p></td>
<td align="left"><p>Nome dell'area di lavoro MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome computer area di lavoro</p></td>
<td align="left"><p>Nome del computer in cui è in uso l'area di lavoro MED-V.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a>Come generare un report del log degli errori


**Per generare un report del log degli errori**

1.  Fare clic sul pulsante Gestione **report** .

2.  Nel menu **tipi di report** del modulo **report** selezionare **log degli errori**e quindi fare clic su **genera**.

3.  Nella finestra di dialogo **parametri report** configurare uno o più dei parametri seguenti:

    -   **Numero di giorni**: il numero di giorni da visualizzare nel report.

    -   **Nome utente contiene**: ogni evento in cui il nome utente contiene il testo immesso è incluso nel report.

    -   **Host Name Contains**: ogni evento in cui il nome host contiene il testo immesso è incluso nel report.

4.  Fai clic su **OK**.

    Viene generato un report con gli eventi e le date selezionati. I parametri del report sono definiti nella tabella seguente.

**Proprietà del report log errori**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Proprietà</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ID evento</p></td>
<td align="left"><p>ID evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Categoria</p></td>
<td align="left"><p>Il modulo a cui fa riferimento il report.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Descrizione dell'evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tempo ricevuto</p></td>
<td align="left"><p>Data e ora in cui l'evento è stato ricevuto nel server.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se il client sta lavorando offline, il server riceve i report quando il client è online.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Nota</strong><br/><p>Per impostazione predefinita, gli eventi vengono visualizzati in ordine di data decrescente. Tuttavia, può essere modificato facendo clic sulla <strong> colonna data/ora ricevuta </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Ora client</p></td>
<td align="left"><p>La data e l'ora in cui si è verificato l'evento in base all'orologio client.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome host</p></td>
<td align="left"><p>Il nome del computer host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome utente</p></td>
<td align="left"><p>L'utente che ha avviato l'evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome area di lavoro</p></td>
<td align="left"><p>Nome dell'area di lavoro MED-V.</p></td>
</tr>
</tbody>
</table>











