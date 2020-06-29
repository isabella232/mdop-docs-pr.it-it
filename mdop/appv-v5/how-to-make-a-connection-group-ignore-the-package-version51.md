---
title: Come impostare un gruppo di connessione in modo che ignori la versione del pacchetto
description: Come impostare un gruppo di connessione in modo che ignori la versione del pacchetto
author: dansimp
ms.assetid: db16b095-dbe2-42c7-863d-b0d5d91b2f4c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 026ef1b3a2aa073a684b1fe5da4f79aa1067072d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805349"
---
# Come impostare un gruppo di connessione in modo che ignori la versione del pacchetto


Microsoft Application Virtualization (App-V) 5,1 consente di configurare un gruppo di connessioni per l'uso di una versione qualsiasi di un pacchetto, semplificando gli aggiornamenti dei pacchetti e riducendo il numero di gruppi di connessione che è necessario creare.

Per aggiornare un pacchetto in alcune versioni precedenti di App-V, è necessario eseguire diversi passaggi, tra cui la disabilitazione del gruppo di connessioni e la modifica del file di definizione XML del gruppo di connessioni.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descrizione delle attività con App-V 5,1</th>
<th align="left">Come eseguire l'attività con App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Puoi configurare un gruppo di connessioni per accettare qualsiasi versione di un pacchetto, che ti consente di aggiornare il pacchetto senza dover disabilitare il gruppo di connessioni.</p>
<p><strong>Funzionamento della caratteristica:</strong></p>
<ul>
<li><p>Se il gruppo di connessioni ha accesso a più versioni di un pacchetto, viene usata la versione più recente.</p></li>
<li><p>Se il gruppo di connessioni contiene un pacchetto facoltativo con una versione non corretta, il pacchetto viene ignorato e non bloccherà l'ambiente virtuale del gruppo di connessioni da creare.</p></li>
<li><p>Se il gruppo di connessioni contiene un pacchetto non facoltativo con una versione non corretta, non è possibile creare l'ambiente virtuale del gruppo di connessioni.</p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo</th>
<th align="left">Passaggi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Server-Console di gestione</p></td>
<td align="left"><ol>
<li><p>Nella console di gestione selezionare <strong> gruppi di connessioni </strong> .</p></li>
<li><p>Selezionare il gruppo di connessioni corretto dalla raccolta gruppi di connessioni.</p></li>
<li><p>Fare clic su <strong> modifica </strong> nel riquadro pacchetti connessi.</p></li>
<li><p>Selezionare <strong> </strong> la casella di controllo Usa qualsiasi versione accanto al nome del pacchetto e fare clic su <strong> Applica </strong> .</p></li>
</ol>
<p>Per altre informazioni sull'aggiunta o l'aggiornamento di pacchetti, vedere <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)"> come aggiungere o aggiornare pacchetti tramite la console di gestione </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client App-V in un computer autonomo</p></td>
<td align="left"><ol>
<li><p>Creare il documento XML del gruppo di connessioni.</p></li>
<li><p>Per aggiornare il pacchetto, imposta l' <strong> </strong> attributo di tag del pacchetto <strong> VersionId </strong> su un asterisco ( <strong>*</strong> ).</p></li>
<li><p>Utilizzare il cmdlet seguente per aggiungere il gruppo di connessioni e includere il percorso del documento XML del gruppo di connessioni:</p>
<p><strong>Add-AppvClientConnectionGroup</strong></p></li>
<li><p>Quando si aggiorna un pacchetto, usare i cmdlet seguenti per rimuovere il pacchetto precedente, aggiungere il pacchetto aggiornato e pubblicare il pacchetto aggiornato:</p>
<ul>
<li><p>RemoveAppvClientPackage</p></li>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Publish-AppvClientPackage</p></li>
</ul></li>
</ol>
<p>Per altre informazioni, vedi:</p>
<ul>
<li><p>File XML di esempio, <strong> file XML del gruppo di connessioni con pacchetti facoltativi </strong> , in questa sezione: <a href="how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional)"> come usare i pacchetti facoltativi nei gruppi di connessioni</a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">Come gestire i pacchetti App-V 5.1 in esecuzione in un computer autonomo con PowerShell</a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## Argomenti correlati


[Gestione dei gruppi di connessione](managing-connection-groups51.md)

 

 





