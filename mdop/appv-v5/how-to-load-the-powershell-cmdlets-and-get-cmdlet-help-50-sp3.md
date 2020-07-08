---
title: Come caricare i cmdlet di PowerShell e ottenere informazioni sui cmdlet
description: Come caricare i cmdlet di PowerShell e ottenere informazioni sui cmdlet
author: dansimp
ms.assetid: 0624495b-943e-485b-9e54-b50e4ee6591c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 7692d3e36aabc4f3142f664e94d9d71b2cfc1bd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805367"
---
# Come caricare i cmdlet di PowerShell e ottenere informazioni sui cmdlet


Argomenti illustrati in questo argomento:

-   [Requisiti per l'uso dei cmdlet di PowerShell](#bkmk-reqs-using-posh)

-   [Caricamento dei cmdlet di PowerShell](#bkmk-load-cmdlets)

-   [Ottenere assistenza per i cmdlet di PowerShell](#bkmk-get-cmdlet-help)

-   [Visualizzazione della Guida per un cmdlet di PowerShell](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a>Requisiti per l'uso dei cmdlet di PowerShell


Esaminare i requisiti seguenti per l'uso dei cmdlet di PowerShell per App-V:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisito</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gli utenti possono eseguire cmdlet App-V Server solo se si concede loro l'accesso usando uno dei metodi seguenti:</p></td>
<td align="left"><ul>
<li><p><strong>Quando si distribuisce e si configura il server App-V </strong> :</p>
<p>Specificare un gruppo di Active Directory o un singolo utente che disponga delle autorizzazioni per la gestione dell'ambiente App-V. Vedere <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> come distribuire il server App-V 5,0 </a> .</p></li>
<li><p><strong>Dopo aver distribuito App-V Server </strong> :</p>
<p>Usare la console di gestione di App-V per aggiungere un altro gruppo o utente di Active Directory. Vedere <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)"> come aggiungere o rimuovere un amministratore tramite la console di gestione </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Cmdlet che richiedono un prompt dei comandi con privilegi elevati</p></td>
<td align="left"><ul>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
<li><p>Set-AppvClientConfiguration</p></li>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Remove-AppvClientConnectionGroup</p></li>
<li><p>Add-AppvPublishingServer</p></li>
<li><p>Remove-AppvPublishingServer</p></li>
<li><p>Send-AppvClientReport</p></li>
<li><p>Set-AppvClientMode</p></li>
<li><p>Set-AppvClientPackage</p></li>
<li><p>Set-AppvPublishingServer</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>I cmdlet che gli utenti finali possono eseguire, a meno che non vengano configurati per richiedere un prompt dei comandi con privilegi elevati</p></td>
<td align="left"><ul>
<li><p>Publish-AppvClientPackage</p></li>
<li><p>Annulla pubblicazione-AppvClientPackage</p></li>
</ul>
<p>Per configurare questi cmdlet in modo da richiedere un prompt dei comandi con privilegi elevati, usare uno di questi metodi:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo</th>
<th align="left">Altre risorse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Eseguire il <strong> cmdlet Set-AppvClientConfiguration </strong> con il <strong> parametro-RequirePublishAsAdmin </strong> .</p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)">Come gestire i gruppi di connessione in un computer autonomo con PowerShell</a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Abilitare l'impostazione di criteri di gruppo "Richiedi pubblica come amministratore" per i client App-V.</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)">Come pubblicare un pacchetto tramite la console di gestione</a> </p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a>Caricamento dei cmdlet di PowerShell
Per caricare i moduli cmdlet di PowerShell:

1.  Aprire Windows PowerShell o Windows PowerShell Integrated Scripting Environment (ISE).

2.  Digitare uno dei comandi seguenti per caricare i cmdlet per il modulo desiderato:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente App-V</th>
<th align="left">Comando per digitare</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Server</p></td>
<td align="left"><p>Import-Module AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sequencer App-V</p></td>
<td align="left"><p>Import-Module AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client App-V</p></td>
<td align="left"><p>Import-Module AppvClient</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-get-cmdlet-help"></a>Ottenere assistenza per i cmdlet di PowerShell
A partire da App-V 5,0 SP3, la guida per i cmdlet è disponibile in due formati:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Come modulo scaricabile</p></td>
<td align="left"><p>Per scaricare la guida più recente dopo il download del modulo cmdlet:</p>
<ol>
<li><p>Aprire Windows PowerShell o Windows PowerShell Integrated Scripting Environment (ISE).</p></li>
<li><p>Digitare uno dei comandi seguenti per caricare i cmdlet per il modulo desiderato:</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente App-V</th>
<th align="left">Comando per digitare</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Server</p></td>
<td align="left"><p>Update-Guida-modulo AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sequencer App-V</p></td>
<td align="left"><p>Update-Guida-modulo AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client App-V</p></td>
<td align="left"><p>Update-Guida-modulo AppvClient</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>In TechNet come pagine Web</p></td>
<td align="left"><p>Vedere il nodo App-V in <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automazione di Microsoft Desktop Optimization Pack con Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-display-help-cmdlet"></a>Visualizzazione della Guida per un cmdlet di PowerShell
Per visualizzare la Guida di un cmdlet di PowerShell specifico:

1.  Aprire Windows PowerShell o Windows PowerShell Integrated Scripting Environment (ISE).

2.  Digitare **Get-Help** &lt; *cmdlet* &gt; , ad esempio **Get-Help Publish-AppvClientPackage**.

**Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V**? Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





