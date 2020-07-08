---
title: Visualizzazione dei metadati di pubblicazione del server App-V
description: Visualizzazione dei metadati di pubblicazione del server App-V
author: dansimp
ms.assetid: d5fa9eb5-647c-478d-8a4d-0ecda018bce6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97c59301678280febe23b8061c08033a88ae49c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804822"
---
# Visualizzazione dei metadati di pubblicazione del server App-V


Usare questa procedura per visualizzare i metadati di pubblicazione, che consentono di risolvere i problemi relativi alla pubblicazione. Per usare questa procedura, è necessario usare app-V Management Server.

Questo articolo contiene le informazioni seguenti:

-   [Requisiti di App-V 5,1 per la visualizzazione dei metadati di pubblicazione](#bkmk-51-reqs-pub-meta)

-   [Sintassi da usare per la visualizzazione dei metadati di pubblicazione](#bkmk-syntax-view-pub-meta)

-   [Valori di query per il sistema operativo client e la versione](#bkmk-values-query-pub-meta)

-   [Definizione dei metadati di pubblicazione](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-51-reqs-pub-meta"></a>Requisiti di App-V 5,1 per la visualizzazione dei metadati di pubblicazione


In App-V 5,1 è necessario specificare i valori seguenti nell'indirizzo quando si esegue una query sul server di pubblicazione App-V per i metadati:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Ulteriori dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p>Se si omette il <strong> </strong> parametro ClientVersion dalla query, i metadati escludono le caratteristiche nuove in App-V 5,0 SP3.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Clientos</strong></p></td>
<td align="left"><p>È necessario specificare questo valore solo se si selezionano sistemi operativi client specifici quando si sequenzia il pacchetto. Se si seleziona l'impostazione predefinita (tutti i sistemi operativi), non specificare questo valore nella query.</p>
<p>Se si omette il <strong> parametro clientos </strong> dalla query, solo i pacchetti sequenziati per supportare qualsiasi sistema operativo verranno visualizzati nei metadati.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a>Sintassi della query per la visualizzazione dei metadati di pubblicazione


Nella tabella seguente sono disponibili gli esempi di sintassi e query.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione di App-V</th>
<th align="left">Sintassi della query</th>
<th align="left">Descrizioni dei parametri</th>
<th align="left">Esempio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3 e App-V 5,1</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
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
<td align="left"><p>&lt;PubServer&gt;</p></td>
<td align="left"><p>Nome del server di pubblicazione App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Porta di pubblicazione #&gt;</p></td>
<td align="left"><p>Porta al server di pubblicazione App-V, definito al momento della configurazione del server di pubblicazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClientVersion = &lt; AppvClientVersion&gt;</p></td>
<td align="left"><p>Versione del client App-V. Fare riferimento alla tabella seguente per il valore corretto da usare.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Clientos = &lt; OSStringValue&gt;</p></td>
<td align="left"><p>Sistema operativo del computer in cui è in uso il client App-V. Fare riferimento alla tabella seguente per il valore corretto da usare.</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p>Per ottenere il nome del server di pubblicazione e il numero di porta (http:// &lt; PubServer &gt; : &lt; Port Publishing # &gt; ) dal client App-V, vedere la configurazione URL del <strong> cmdlet Get-AppvPublishingServer di </strong> PowerShell.</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p>Nell'esempio:</p>
<ul>
<li><p>Un Windows Server 2012 R2 denominato "pubsvr01" ospita il servizio di pubblicazione.</p></li>
<li><p>Il client Windows è Windows 8,1 64 bit.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0 tramite App-V 5,0 SP2</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong>Nota</strong><br/><p><strong>ClientVersion </strong> e <strong> clientos </strong> sono supportati solo in app-v 5,0 SP3 e app-v 5,1.</p>
</div>
<div>

</div></td>
<td align="left"><p>Vedere le informazioni per App-V 5,0 SP3 e App-V 5,1.</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p>Nell'esempio, un Windows Server 2012 R2 denominato "pubsvr01" ospita i servizi di gestione e pubblicazione.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a>Valori di query per il sistema operativo client e la versione


Nella query di metadati di pubblicazione immettere i valori stringa che corrispondono al sistema operativo client e alla versione in uso.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Architettura</th>
<th align="left">Valore stringa di stringa operativa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows10</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>WindowsClient_10.0_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows10</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>WindowsClient_10.0_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>WindowsClient_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>WindowsClient_6.1_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>WindowsServer_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>WindowsServer_6.1_x86</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a>Definizione dei metadati di pubblicazione


Quando i pacchetti vengono pubblicati in un computer che esegue App-V client, i metadati vengono inviati al computer che indica i pacchetti e i gruppi di connessioni da pubblicare. Il client App-V effettua due richieste separate per le seguenti:

-   Pacchetti e gruppi di connessioni autorizzati al computer client.

-   Pacchetti e gruppi di connessioni autorizzati all'utente corrente.

Il server di pubblicazione comunica con il server di gestione per determinare i pacchetti e i gruppi di connessioni disponibili per il richiedente. Il server di pubblicazione deve essere registrato con il server di gestione in modo che i metadati vengano generati.

È possibile visualizzare i metadati per ogni richiesta in un browser Internet usando una query nel contesto dell'utente o del computer specifico.






## Argomenti correlati


[Documentazione tecnica per App-V 5.1](technical-reference-for-app-v-51.md)









