---
title: Prerequisiti di App-V 5.0
description: Prerequisiti di App-V 5.0
author: dansimp
ms.assetid: 9756b571-c785-4ce6-a95c-d4e134e89429
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 176c9729d8c909325c6d6694e024938d9ce9df53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806009"
---
# Prerequisiti di App-V 5.0

Prima di iniziare la configurazione di Microsoft Application Virtualization (App-V) 5,0, è necessario assicurarsi di avere soddisfatto i prerequisiti per installare il prodotto. Questo argomento contiene informazioni utili per pianificare correttamente la preparazione dell'ambiente di elaborazione prima di distribuire le caratteristiche dell'App-V 5,0.

> [!Important]
> **I prerequisiti in questo articolo si applicano solo a App-V 5,0**. Per i prerequisiti aggiuntivi che si applicano ai Service Pack App-V 5,0, vedere le pagine Web seguenti:

-   [Novità in App-V 5.0 SP1](whats-new-in-app-v-50-sp1.md)

-   [Informazioni su App-V 5.0 SP2](about-app-v-50-sp2.md)

-   [Prerequisiti di App-V 5.0 SP3](app-v-50-sp3-prerequisites.md)

La tabella seguente elenca le informazioni sui prerequisiti relative a sistemi operativi specifici.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistemi operativi</th>
<th align="left">Descrizione del requisito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Computer in cui è in uso:</p>
<ul>
<li><p>Windows 8</p></li>
<li><p>Windows Server 2012</p></li>
</ul></td>
<td align="left"><p>I prerequisiti seguenti sono già installati:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5-non è necessario Microsoft .NET Framework 4</p></li>
<li><p>Windows PowerShell 3,0</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Computer in cui è in uso:</p>
<ul>
<li><p>Windows 7</p></li>
<li><p>Windows Server 2008</p></li>
</ul></td>
<td align="left"><p>È consigliabile scaricare la KB seguente:</p>
<p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[Microsoft Security Advisory: Insecure library loading could allow remote code execution](https://support.microsoft.com/kb/2533623)">Advisory Microsoft sulla sicurezza: il caricamento della raccolta non sicuro può consentire l'esecuzione di codice remoto</a></p>
<p>Assicurati di verificare la presenza di KBs successive che hanno sostituito questo uno e tieni presente che alcuni KBs potrebbero richiedere la disinstallazione degli aggiornamenti precedenti.</p></td>
</tr>
</tbody>
</table>

## Prerequisiti di installazione per l'App-V 5,0

> [!Note]  
> I prerequisiti seguenti sono già installati per i computer che eseguono Windows 8.

Ogni funzionalità di App-V 5,0 include prerequisiti specifici che devono essere soddisfatti prima che le funzionalità dell'App-V 5,0 possano essere installate correttamente.

### Prerequisiti per il client App-V 5,0

La tabella seguente elenca i prerequisiti di installazione per il client App-V 5,0:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Requisiti software</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacchetto completo)</p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p>
<div class="alert">
<strong>Nota</strong><br/><p>L'installazione di PowerShell 3,0 richiede un riavvio.</p>
</div>
<div>

</div></li>
<li><p>Scaricare e installare <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>È possibile scaricare e installare l'articolo precedente della Knowledge. Tuttavia, potrebbe essere stato sostituito con una versione più recente.</p>
</div>
<div>

</div></li>
<li><p>Il programma di installazione client (con estensione exe) rileverà se è necessario installare i prerequisiti seguenti e lo farà di conseguenza:</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacchetti ridistribuibili di Visual C++ per Visual Studio 2013</a></p>
<p>Questo prerequisito è obbligatorio solo se è stato installato il pacchetto hotfix 4 per Application Virtualization 5,0 SP2 o versione successiva.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">Microsoft Visual C++ 2010 ridistribuibile</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Pacchetto ridistribuibile di Microsoft Visual C++ 2005 SP1 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Prerequisiti per il client di Servizi Desktop remoto App-V 5,0

> [!Note]  
> I prerequisiti seguenti sono già installati per i computer che eseguono Windows Server 2012.

La tabella seguente elenca i prerequisiti di installazione per il client di Servizi Desktop remoto App-V 5,0:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Requisiti software</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft.NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft.NET Framework 4 (pacchetto completo)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p>
<div class="alert">
<strong>Nota</strong><br/><p>L'installazione di PowerShell 3,0 richiede un riavvio.</p>
</div>
<div>

</div></li>
<li><p>Scaricare e installare <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>È possibile scaricare e installare l'articolo precedente della Knowledge. Tuttavia, potrebbe essere stato sostituito con una versione più recente.</p>
</div>
<div>

</div></li>
<li><p>Il programma di installazione client (. exe) rileverà se è necessario installare i prerequisiti seguenti e lo farà di conseguenza:</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacchetti ridistribuibili di Visual C++ per Visual Studio 2013</a></p>
<p>Questo requisito è obbligatorio solo se è stato installato il pacchetto hotfix 4 per Application Virtualization 5,0 SP2 o versione successiva.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">Microsoft Visual C++ 2010 ridistribuibile</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Pacchetto ridistribuibile di Microsoft Visual C++ 2005 SP1 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Prerequisiti per il sequencer App-V 5,0

> [!Note]
> I prerequisiti seguenti sono già installati per i computer che eseguono Windows 8 e Windows Server 2012.

La tabella seguente elenca i prerequisiti di installazione per l'App-V 5,0 sequencer. Se possibile, il computer che esegue il Sequencer deve avere le stesse configurazioni hardware e software dei computer che eseguono le applicazioni virtuali.

> [!Note]  
> Se i requisiti di sistema di un'applicazione installata localmente superano i requisiti del sequencer, è necessario soddisfare i requisiti di tale applicazione. Inoltre, dato che il processo di sequenziazione è intensivo di risorse di sistema, è consigliabile che il computer che esegue il sequencer abbia abbondanza di memoria, un processore veloce e un disco rigido veloce. Per altre informazioni, Vedi [configurazioni supportate in App-V 5,0](app-v-50-supported-configurations.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Requisiti software</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacchetti ridistribuibili di Visual C++ per Visual Studio 2013</a></p>
<p>Questo requisito è obbligatorio solo se è stato installato il pacchetto hotfix 4 per Application Virtualization 5,0 SP2.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacchetto completo)</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></li>
<li><p>Scaricare e installare <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p></li>
<li><p>Per i computer che eseguono Microsoft Windows Server 2008 R2 SP1, scaricare e installare <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>È possibile scaricare e installare uno degli articoli della Knowledge versione precedenti. Tuttavia, potrebbero essere stati sostituiti con una versione più recente.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
</tbody>
</table>

### Prerequisiti per il server App-V 5,0

> [!Note]
> I prerequisiti seguenti sono già installati per i computer che eseguono Windows Server 2012:

-   Microsoft .NET Framework 4,5. In questo articolo vengono eliminati i requisiti di Microsoft .NET Framework 4.

-   Windows PowerShell 3,0

-   Scaricare e installare [KB2533623](https://support.microsoft.com/kb/2533623) (https://support.microsoft.com/kb/2533623)

    > [!Important]
    > È comunque possibile scaricare l'installazione della KB precedente. Tuttavia, potrebbe essere stato sostituito con una versione più recente.

La tabella seguente elenca i prerequisiti di installazione per il server App-V 5,0. L'account usato per installare i componenti del server deve avere diritti amministrativi nel computer in cui si sta eseguendo l'installazione. Questo account deve anche avere la possibilità di eseguire query sui servizi directory di Active Directory. Prima di installare e configurare i server App-V 5,0, è necessario specificare una porta in cui verranno ospitati tutti i componenti. Devi anche aggiungere le regole del firewall associate per consentire le richieste in arrivo alle porte specificate.

> [!Note]
> WebDAV (Web Distributed Authoring and Versioning) viene disabilitato automaticamente per il servizio di gestione.

Il server App-V 5,0 è supportato per una distribuzione autonoma, in cui tutti i componenti sono distribuiti nello stesso server e una distribuzione distribuita. A seconda della topologia usata per distribuire il server App-V 5,0, i dati necessari per ogni componente cambieranno leggermente.

> [!Important]
> L'installazione del server App-V 5,0 in un computer che esegue qualsiasi versione o componente precedente di App-V non è supportata. Inoltre, l'installazione dei componenti del server in un computer che esegue Core Server o un controller di dominio non è supportata.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Server di gestione</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacchetto completo)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<div class="alert">
<strong>Nota</strong><br/><p>L'installazione di PowerShell 3,0 richiede un riavvio.</p>
</div>
<div>

</div></li>
<li><p>Windows Web Server con il ruolo IIS abilitato e le caratteristiche seguenti: <strong> Caratteristiche HTTP comuni </strong> (contenuto statico e documento predefinito), <strong> sviluppo di applicazioni </strong> (ASP.NET, estensibilità .NET, estensioni ISAPI e filtri ISAPI), <strong> sicurezza </strong> (autenticazione di Windows, filtro delle richieste), <strong> strumenti di gestione </strong> (console di gestione di IIS).</p></li>
<li><p>Scaricare e installare <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>È comunque possibile scaricare l'installazione della KB precedente. Tuttavia, potrebbe essere stato sostituito con una versione più recente.</p>
</div>
<div>

</div></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=13523" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x64)](https://www.microsoft.com/download/details.aspx?id=13523)">Pacchetto ridistribuibile di Microsoft Visual C++ 2010 SP1 (x64)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Pacchetto ridistribuibile di Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><p>registrazione ASP.NET di 64 bit</p></li>
</ul>
<p>I componenti del server App-V 5,0 sono dipendenti, ma hanno requisiti e opzioni di installazione diversi che devono essere distribuiti. Usare le informazioni seguenti per preparare l'ambiente per l'esecuzione del server di gestione di App-V 5,0.</p>
<ul>
<li><p>Posizione di installazione: per impostazione predefinita, questo componente verrà installato in <strong> %Programmi%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Posizione del database di gestione di App-V 5,0-nome di SQL Server, nome dell'istanza SQL, nome del database.</p></li>
<li><p>Diritti di accesso per la console di gestione di App-V 5,0: l'utente o il gruppo a cui deve essere concesso l'accesso alla console di gestione alla fine della distribuzione. Dopo la distribuzione, solo questi utenti avranno accesso alla console di gestione finché non verranno aggiunti altri amministratori tramite la console di gestione.</p>
<div class="alert">
<strong>Nota</strong><br/><p>I gruppi di sicurezza e i singoli utenti non sono supportati. Devi specificare un gruppo di servizi di dominio Active Directory.</p>
</div>
<div>

</div></li>
<li><p>Nome sito Web del servizio di gestione di App-V 5,0: specificare un nome per il sito Web o usare il nome predefinito.</p></li>
<li><p>Binding della porta del servizio di gestione di App-V 5,0-deve essere un numero di porta univoco che non viene usato da un altro sito Web nel computer.</p></li>
<li><p>Supporto per Microsoft Silverlight: è necessario installare Microsoft Silverlight prima della disponibilità della console di gestione. Anche se non si tratta di un requisito per la distribuzione, il server deve essere in grado di supportare Microsoft Silverlight.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Database di gestione</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Nota</strong><br/><p>Il database è obbligatorio solo quando si usa l'App-V 5,0 Management Server.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacchetto completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Pacchetto ridistribuibile di Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
</ul>
<p>I componenti del server App-V 5,0 sono dipendenti, ma hanno requisiti e opzioni di installazione diversi che devono essere distribuiti. Usare le informazioni seguenti per preparare l'ambiente per l'esecuzione del database di gestione di App-V 5,0.</p>
<ul>
<li><p>Posizione di installazione-per impostazione predefinita, questo componente verrà installato in <strong> %Programmi%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nome istanza di SQL Server personalizzata (se applicabile): il formato deve essere <strong> InstanceName </strong> , perché l'installazione presuppone che si trovi nel computer locale. Se specifichi il nome con il formato seguente, <strong> SVR\INSTANCE </strong> avrà esito negativo.</p></li>
<li><p>Nome database App-V 5,0 personalizzato (se applicabile): è necessario specificare un nome di database univoco. Il valore predefinito per il database di gestione è <strong> AppVManagement </strong> .</p></li>
<li><p>Posizione del server di gestione di App-V 5,0: specifica l'account del computer in cui è distribuito il server di gestione. Questa operazione deve essere specificata con il formato seguente <strong> Domain\MachineAccount </strong> .</p></li>
<li><p>Amministratore dell'installazione di App-V 5,0 Management Server-specifica l'account che verrà usato per installare l'App-V 5,0 Management Server. È consigliabile usare il formato seguente: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Microsoft SQL Server Service Agent-configura il computer che gestisce il database di gestione di App-V 5,0 in modo che il servizio Microsoft SQL Server Agent venga riavviato automaticamente. Per altre informazioni, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=273725" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://go.microsoft.com/fwlink/?LinkId=273725)"> configurare SQL Server Agent per riavviare i servizi automaticamente</a></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Server di report</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacchetto completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Pacchetto ridistribuibile di Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><div class="alert">
<strong>Nota</strong><br/><p>Per ridurre il rischio di invio di dati indesiderati o malintenzionati al server di report, è necessario limitare l'accesso al servizio Web Reporting per i criteri di sicurezza aziendali.</p>
</div>
<div>

</div>
<p>Windows Web Server con il ruolo IIS con le caratteristiche seguenti: <strong> Caratteristiche HTTP comuni </strong> (contenuto statico e documento predefinito), <strong> sviluppo di applicazioni </strong> (ASP.NET, estensibilità .NET, estensioni ISAPI e filtri ISAPI), <strong> sicurezza </strong> (autenticazione di Windows, filtro delle richieste), <strong> sicurezza </strong> (autenticazione di Windows, filtro delle richieste), <strong> strumenti di gestione </strong> (console di gestione di IIS)</p></li>
<li><p>registrazione ASP.NET di 64 bit</p></li>
<li><p>Posizione di installazione-per impostazione predefinita, questo componente viene installato in <strong> %Programmi%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nome sito Web del servizio di Reporting di App-V 5,0-specifica il nome del sito Web o il nome predefinito che verrà usato.</p></li>
<li><p>Binding della porta del servizio report di App-V 5,0-deve essere un numero di porta univoco non già usato da un altro sito Web che viene eseguito nel computer.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Database di report</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Nota</strong><br/><p>Il database è obbligatorio solo quando si usa l'App-V 5,0 Reporting Server.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacchetto completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Pacchetto ridistribuibile di Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
</ul>
<p>I componenti del server App-V 5,0 sono dipendenti, ma hanno requisiti e opzioni di installazione diversi che devono essere distribuiti. Usare le informazioni seguenti per preparare l'ambiente per l'esecuzione del database di report App-V 5,0.</p>
<ul>
<li><p>Posizione di installazione-per impostazione predefinita, questo componente verrà installato in <strong> %Programmi%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nome istanza di SQL Server personalizzata (se applicabile): il formato deve essere <strong> InstanceName </strong> , perché l'installazione presuppone che si trovi nel computer locale. Se specifichi il nome con il formato seguente, <strong> SVR\INSTANCE </strong> avrà esito negativo.</p></li>
<li><p>Nome database App-V 5,0 personalizzato (se applicabile): è necessario specificare un nome di database univoco. Il valore predefinito per il database di report è <strong> AppVReporting </strong> .</p></li>
<li><p>Posizione del server di Reporting di App-V 5,0: specifica l'account del computer in cui è distribuito il server di report. Questa operazione deve essere specificata con il formato seguente <strong> Domain\MachineAccount </strong> .</p></li>
<li><p>App-V 5,0 Administrator per l'installazione di Reporting Server-specifica l'account che verrà usato per installare l'App-V 5,0 Reporting Server. È consigliabile usare il formato seguente: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Servizio Microsoft SQL Server e servizio Microsoft SQL Server Agent: questi servizi devono essere associati agli account utente che hanno accesso a query AD.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Server di pubblicazione</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacchetto completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Pacchetto ridistribuibile di Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><p>Windows Web Server con il ruolo IIS con le caratteristiche seguenti: <strong> Caratteristiche HTTP comuni </strong> (contenuto statico e documento predefinito), <strong> sviluppo di applicazioni </strong> (ASP.NET, estensibilità .NET, estensioni ISAPI e filtri ISAPI), <strong> sicurezza </strong> (autenticazione di Windows, filtro delle richieste), <strong> sicurezza </strong> (autenticazione di Windows, filtro delle richieste), <strong> strumenti di gestione </strong> (console di gestione di IIS)</p></li>
<li><p>registrazione ASP.NET di 64 bit</p></li>
</ul>
<p>I componenti del server App-V 5,0 sono dipendenti, ma hanno requisiti e opzioni di installazione diversi che devono essere distribuiti. Usare le informazioni seguenti per preparare l'ambiente per l'esecuzione del server di pubblicazione App-V 5,0.</p>
<ul>
<li><p>Posizione di installazione-per impostazione predefinita, questo componente viene installato in <strong> %Programmi%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>URL del servizio di gestione di App-V 5,0: specifica l'URL del servizio di gestione di App-V 5,0. Questa è la porta con cui viene comunicato il server di pubblicazione e deve essere specificata usando il formato seguente: <strong><a href="http://localhost:12345" data-raw-source="http://localhost:12345"> http://localhost:12345 </a></strong> .</p></li>
<li><p>Nome sito Web del servizio di pubblicazione App-V 5,0-specifica il nome del sito Web o il nome predefinito che verrà usato.</p></li>
<li><p>Binding della porta del servizio di pubblicazione App-V 5,0-deve essere un numero di porta univoco non già usato da un altro sito Web che viene eseguito nel computer.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Argomenti correlati

[Pianificazione della distribuzione di App-V](planning-to-deploy-app-v.md)

[Configurazioni supportate di App-V 5.0](app-v-50-supported-configurations.md)
