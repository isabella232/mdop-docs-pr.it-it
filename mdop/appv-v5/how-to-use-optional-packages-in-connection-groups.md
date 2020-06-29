---
title: Come usare i pacchetti facoltativi nei gruppi di connessione
description: Come usare i pacchetti facoltativi nei gruppi di connessione
author: dansimp
ms.assetid: 4d08a81b-55e5-471a-91dc-9a684fb3c9a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 64a2c0758294bfa617d3d85f888cfce3a2c0d21e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805122"
---
# Come usare i pacchetti facoltativi nei gruppi di connessione


A partire da Microsoft Application Virtualization (App-V) 5,0 SP3, è possibile aggiungere pacchetti facoltativi ai gruppi di connessioni per semplificare la gestione dei gruppi di connessioni. La tabella seguente riepiloga le attività che è possibile completare più facilmente con i pacchetti facoltativi e fornisce collegamenti alle istruzioni per ogni attività.

**Nota** 
 **I pacchetti facoltativi sono supportati solo in App-V 5,0 SP3.**

 

Prima di usare pacchetti facoltativi, vedere [requisiti per l'uso di pacchetti facoltativi nei gruppi di connessioni](#bkmk-reqs-using-cg).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Collegamento alle istruzioni</th>
<th align="left">Attività</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)">Usare un gruppo di connessioni, con pacchetti facoltativi, per più utenti con pacchetti diversi a cui hanno diritto</a></p></td>
<td align="left"><p>Usa un singolo gruppo di connessioni per creare diversi gruppi di applicazioni e plug-in disponibili per diversi utenti finali.</p>
<p>Ad esempio, si vuole distribuire Microsoft Office a tutti gli utenti finali, ma distribuire plug-in diversi a diversi sottoinsiemi di utenti.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)">Annullare la pubblicazione o eliminare un pacchetto facoltativo oppure annullare la pubblicazione di un pacchetto facoltativo e ripubblicarlo in un secondo momento senza modificare il gruppo di connessioni</a></p></td>
<td align="left"><p>Annullare la pubblicazione, eliminare o ripubblicare un pacchetto facoltativo senza dover disabilitare, rimuovere, modificare, aggiungere e riattivare il gruppo di connessioni nel client App-V.</p>
<p>È anche possibile annullare la pubblicazione del pacchetto facoltativo e ripubblicarlo in un secondo momento senza dover disabilitare o ripubblicare il gruppo di connessioni.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a>Usare un gruppo di connessioni, con pacchetti facoltativi, per più utenti con pacchetti diversi a cui hanno diritto


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descrizione attività</th>
<th align="left">Come eseguire l'attività</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Con App-V 5,0 SP3</strong></p>
<p>È possibile aggiungere pacchetti facoltativi ai gruppi di connessioni, che consente di specificare combinazioni diverse di applicazioni e plug-in per diversi utenti finali.</p>
<p><strong>Esempio </strong> : si vuole distribuire Microsoft Office agli utenti finali, ma abilitare un determinato plug-in solo per un sottoinsieme di utenti.</p>
<p>A questo scopo, crea un gruppo di connessioni che contiene un pacchetto con Office e un altro pacchetto con plug-in di Office e quindi rendi facoltativo il pacchetto plug-in.</p>
<p>Gli utenti finali che non hanno diritto al pacchetto di plug-in saranno comunque in grado di eseguire Office.</p></td>
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
<li><p>Nella console di gestione selezionare <strong> pacchetti </strong> per aprire la pagina pacchetti.</p></li>
<li><p>Selezionare <strong> gruppi </strong> di connessioni per visualizzare la raccolta gruppi di connessioni.</p></li>
<li><p>Selezionare il gruppo di connessioni corretto dalla raccolta gruppi di connessioni.</p></li>
<li><p>Fare clic su <strong> modifica </strong> nel riquadro pacchetti connessi.</p></li>
<li><p>Selezionare <strong> facoltativo </strong> accanto al nome del pacchetto.</p></li>
<li><p>Selezionare la <strong> casella di controllo Aggiungi pacchetto Access to Group Access </strong> . Questo passaggio necessario aggiunge al gruppo di connessioni i diritti di pacchetto configurati in precedenza quando si assegnavano pacchetti a gruppi di Active Directory.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>App-V Server-cmdlet di PowerShell</p></td>
<td align="left"><p>Usa il cmdlet seguente e specifica il <strong> parametro-Optional </strong> :</p>
<p><strong>Add-AppvServerConnectionGroupPackage</strong></p>
<p><strong>Sintassi</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong>Esempio:</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client App-V in un computer autonomo</p></td>
<td align="left"><ol>
<li><p>Creare il documento XML del gruppo di connessioni e impostare <strong> l' </strong> attributo di tag del pacchetto <strong> </strong> su <strong> "true".</strong></p></li>
<li><p>Usare i cmdlet seguenti per aggiungere e abilitare il gruppo di connessioni:</p>
<ul>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Enable-AppvClientConnectionGroup</p></li>
</ul></li>
</ol>
<p><strong>Esempio di documento XML del gruppo di connessioni con pacchetti facoltativi:</strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Versioni precedenti all'App-V 5,0 SP3</strong></p></td>
<td align="left"><p>È stato necessario creare molti gruppi di connessioni per rendere disponibili le combinazioni di applicazioni e plug-in specifiche per gli utenti specifici.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a>Annullare la pubblicazione o eliminare un pacchetto facoltativo oppure annullare la pubblicazione di un pacchetto facoltativo e ripubblicarlo in un secondo momento senza modificare il gruppo di connessioni


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descrizione attività</th>
<th align="left">Come eseguire l'attività</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Con App-V 5,0 SP3</strong></p>
<p>È possibile annullare la pubblicazione, eliminare o ripubblicare un pacchetto facoltativo, che si trova in un gruppo di connessioni, senza dover disabilitare o riabilitare il gruppo di connessioni nel client App-V.</p>
<p>È anche possibile annullare la pubblicazione di un pacchetto facoltativo e ripubblicarlo in un secondo momento senza dover disabilitare o ripubblicare il gruppo di connessioni.</p>
<p><strong>Esempio </strong> : se si pubblica un pacchetto facoltativo che contiene un plug-in di Microsoft Office e si vuole rimuovere il plug-in, è possibile annullare la pubblicazione del pacchetto senza dover disabilitare il gruppo di connessioni.</p></td>
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
<td align="left"><ul>
<li><p>Per annullare la pubblicazione del pacchetto: nella console di gestione selezionare elegge la <strong> </strong> pagina pacchetti, fare clic con il pulsante destro del mouse sul pacchetto che si vuole annullare la pubblicazione e quindi scegliere <strong> Annulla pubblicazione </strong> .</p></li>
<li><p>Per rimuovere un pacchetto facoltativo da un gruppo di connessioni: nella <strong> pagina gruppi di connessioni </strong> selezionare il pacchetto che si vuole rimuovere e fare clic sulla freccia destra per rimuovere il pacchetto dal riquadro del gruppo di connessioni in basso a sinistra.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Client App-V in un computer autonomo</p></td>
<td align="left"><p>Usare i cmdlet esistenti seguenti:</p>
<ul>
<li><p>Annulla pubblicazione-AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
</ul>
<p>Per altre informazioni, vedere <a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> come gestire i pacchetti App-V 5,0 in uso in un computer autonomo usando PowerShell </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Versioni precedenti all'App-V 5,0 SP3</strong></p></td>
<td align="left"><p>È necessario:</p>
<ol>
<li><p>Rimuovere il gruppo di connessioni da ogni computer client App-V in cui è stato abilitato.</p></li>
<li><p>Annullare la pubblicazione del pacchetto.</p></li>
<li><p>Rimuovere il pacchetto dalla definizione del gruppo di connessioni.</p></li>
<li><p>Ripubblicare il gruppo di connessioni.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a>Requisiti per l'uso di pacchetti facoltativi nei gruppi di connessioni


Verificare i requisiti seguenti prima di usare pacchetti facoltativi nei gruppi di connessioni:

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
<td align="left"><p>I gruppi di connessioni devono contenere almeno un pacchetto non facoltativo.</p></td>
<td align="left"><ul>
<li><p>Verificare attentamente che soddisfi questo requisito, poiché il server App-V e il cmdlet di PowerShell non convalidano che il requisito sia stato soddisfatto.</p></li>
<li><p>Se si crea accidentalmente un gruppo di connessioni che non contiene almeno un pacchetto non facoltativo e l'utente finale prova ad aprire un'applicazione di pacchetto in tale gruppo di connessioni, il gruppo di connessioni non riuscirà.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>I gruppi di connessioni pubblicati dall'utente possono contenere pacchetti pubblicati a livello globale o per l'utente.</p></li>
<li><p>I gruppi di connessioni pubblicati globalmente devono contenere solo pacchetti pubblicati globalmente.</p></li>
</ul></td>
<td align="left"><p>I gruppi di connessioni pubblicati globalmente devono contenere pacchetti pubblicati globalmente per verificare che i pacchetti siano disponibili all'avvio dell'ambiente virtuale del gruppo di connessioni.</p>
<p>Se si tenta di aggiungere o abilitare gruppi di connessioni pubblicati a livello globale che contengono pacchetti pubblicati dall'utente, il gruppo di connessioni non riuscirà.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>È necessario pubblicare tutti i pacchetti non facoltativi prima di pubblicare il gruppo di connessioni che contiene questi pacchetti.</p></td>
<td align="left"><p>L'ambiente virtuale di un gruppo di connessioni non può essere avviato se mancano pacchetti non facoltativi.</p>
<p>Il client App-V non riesce ad aggiungere o abilitare un gruppo di connessioni se i pacchetti non facoltativi non sono stati pubblicati.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Prima di annullare la pubblicazione di un pacchetto pubblicato a livello globale, verificare che i gruppi di connessioni che hanno diritto a tutti gli utenti del computer non richiedano più il pacchetto.</p></td>
<td align="left"><p>Il sistema non controlla se il pacchetto fa parte del gruppo di connessioni di un altro utente. L'annullamento della pubblicazione di un pacchetto globale lo rende non disponibile per tutti gli utenti del computer, quindi assicurati che i gruppi di connessioni di ogni utente non contengano più il pacchetto o in alternativa Rendi il pacchetto facoltativo.</p></td>
</tr>
</tbody>
</table>

 






## Argomenti correlati


[Gestione dei gruppi di connessione](managing-connection-groups.md)

 

 





