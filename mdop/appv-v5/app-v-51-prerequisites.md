---
title: Prerequisiti di App-V 5.1
description: Prerequisiti di App-V 5.1
author: dansimp
ms.assetid: 1bfa03c1-a4ae-45ec-8a2b-b10c2b94bfb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a74d8f8d7148cdb6c32bcafa87f479d24305af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805955"
---
# Prerequisiti di App-V 5.1


Prima di installare Microsoft Application Virtualization (App-V) 5,1, verificare di avere installato tutti i seguenti requisiti software necessari.

Per un elenco dei requisiti hardware e sistemi operativi supportati per App-V Server, sequencer e client, Vedi [configurazioni supportate in App-v 5,1](app-v-51-supported-configurations.md).

## Riepilogo del software preinstallato in ogni sistema operativo


La tabella seguente indica il software già installato per diversi sistemi operativi.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Descrizione del requisito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows10</p></td>
<td align="left"><p>Tutti i prerequisiti software sono già installati.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Tutti i prerequisiti software sono già installati.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se si esegue Windows 8, eseguire l'aggiornamento a Windows 8,1 prima di usare app-V 5,1.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Il software prerequisito seguente è già installato:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5</p></li>
<li><p>Windows PowerShell 3,0</p>
<div class="alert">
<strong>Nota</strong><br/><p>L'installazione di PowerShell 3,0 richiede un riavvio.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Il software prerequisito non è già installato. È necessario installarlo prima di poter installare App-V.</p></td>
</tr>
</tbody>
</table>



## Software prerequisiti App-V Server


Installare il software prerequisito necessario per i componenti del server App-V 5,1.

### Informazioni da conoscere prima di iniziare

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Account per l'installazione di App-V Server</p></td>
<td align="left"><p>L'account usato per installare i componenti di App-V Server deve avere:</p>
<ul>
<li><p>Diritti amministrativi nel computer in cui si stanno installando i componenti.</p></li>
<li><p>Possibilità di eseguire query sui servizi di dominio Active Directory.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Porta e firewall</p></td>
<td align="left"><ul>
<li><p>Specificare una porta in cui verranno ospitati tutti i componenti.</p></li>
<li><p>Aggiungere le regole del firewall associate per consentire le richieste in arrivo alle porte specificate.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>WebDAV (Web Distributed Authoring and Versioning)</p></td>
<td align="left"><p>WebDAV viene disabilitato automaticamente per il servizio di gestione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scenari di distribuzione supportati</p></td>
<td align="left"><ul>
<li><p>Una distribuzione autonoma, in cui tutti i componenti sono distribuiti nello stesso server.</p></li>
<li><p>Distribuzione distribuita.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Scenari di distribuzione non supportati</p></td>
<td align="left"><ul>
<li><p>Installazione di istanze affiancate di più versioni di App-V Server nello stesso server.</p></li>
<li><p>Installare i componenti di App-V Server in un computer che esegue Core Server o Domain controller.</p></li>
</ul></td>
</tr>
</tbody>
</table>



### Software prerequisiti di Management Server

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti e impostazioni obbligatorie</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Versione supportata di SQL Server</p></td>
<td align="left"><p>Per le versioni supportate, vedere <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurazioni supportate in App-V 5,1 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p></td>
<td align="left"><p>L'installazione di PowerShell 3,0 richiede un riavvio.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scaricare e installare <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p></td>
<td align="left"><p>Si applica solo a Windows 7.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacchetti ridistribuibili di Visual C++ per Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>registrazione ASP.NET di 64 bit</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ruolo di Windows Server Web Server</p></td>
<td align="left"><p>Questo ruolo deve essere aggiunto a un sistema operativo server supportato per il server di gestione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Strumenti di gestione di Web Server (IIS)</p></td>
<td align="left"><p>Fare clic su <strong> script e strumenti di gestione IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Servizi ruolo server Web</p></td>
<td align="left"><p><strong>Caratteristiche HTTP comuni:</strong></p>
<ul>
<li><p>Contenuto statico</p></li>
<li><p>Documento predefinito</p></li>
</ul>
<p><strong>Sviluppo di applicazioni:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Estensibilità .NET</p></li>
<li><p>Estensioni ISAPI</p></li>
<li><p>Filtri ISAPI</p></li>
</ul>
<p><strong>Sicurezza</strong></p>
<ul>
<li><p>Autenticazione di Windows</p></li>
<li><p>Filtro delle richieste</p></li>
</ul>
<p><strong>Strumenti di gestione:</strong></p>
<ul>
<li><p>Console di gestione di IIS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Posizione di installazione predefinita</p></td>
<td align="left"><p>%Programmi%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Posizione del database di gestione</p></td>
<td align="left"><p>Nome database di SQL Server, nome istanza database di SQL Server e nome database.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Autorizzazioni della console di gestione e del database di gestione</p></td>
<td align="left"><p>Un utente o un gruppo che può accedere alla console di gestione e al database dopo il completamento della distribuzione. Solo questi utenti o gruppi avranno accesso alla console di gestione e al database, a meno che non vengano aggiunti altri amministratori tramite la console di gestione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome sito Web del servizio di gestione</p></td>
<td align="left"><p>Nome per il sito Web della console di gestione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Binding della porta del servizio di gestione</p></td>
<td align="left"><p>Numero di porta univoco per il servizio di gestione. Questa porta non può essere usata da un altro processo nel computer.</p></td>
</tr>
</tbody>
</table>



**Importante**  
JavaScript deve essere abilitato nel browser che apre la console di gestione Web.



### Software per i prerequisiti del database di Management Server

Il database di gestione è obbligatorio solo se si usa l'App-V 5,1 Management Server.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti e impostazioni obbligatorie</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacchetti ridistribuibili di Visual C++ per Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Posizione di installazione predefinita</p></td>
<td align="left"><p>%Programmi%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome istanza di SQL Server personalizzata (se applicabile)</p></td>
<td align="left"><p>Formato da usare: <strong> InstanceName</strong></p>
<p>Questo formato si basa sul presupposto che l'installazione si trovi nel computer locale.</p>
<p>Se specifichi il nome con il formato <strong> SVR\INSTANCE </strong> , l'installazione non riuscirà.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome database personalizzato (se applicabile)</p></td>
<td align="left"><p>Nome database univoco.</p>
<p>Impostazione predefinita: AppVManagement</p></td>
</tr>
<tr class="even">
<td align="left"><p>Posizione del server di gestione</p></td>
<td align="left"><p>Account del computer in cui è distribuito il server di gestione.</p>
<p>Formato da usare: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Amministratore dell'installazione di server di gestione</p></td>
<td align="left"><p>Account usato per installare il server di gestione.</p>
<p>Formato da usare: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Agente di servizio Microsoft SQL Server</p></td>
<td align="left"><p>Configurare il computer di database di gestione in modo che il servizio Microsoft SQL Server Agent venga riavviato automaticamente. Per istruzioni, vedere <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> configurare SQL Server Agent per riavviare i servizi automaticamente </a> .</p></td>
</tr>
</tbody>
</table>



### Software prerequisito del server di pubblicazione

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti e impostazioni obbligatorie</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacchetti ridistribuibili di Visual C++ per Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>registrazione ASP.NET di 64 bit</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Ruolo di Windows Server Web Server</p></td>
<td align="left"><p>Questo ruolo deve essere aggiunto a un sistema operativo server supportato per il server di gestione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Strumenti di gestione di Web Server (IIS)</p></td>
<td align="left"><p>Fare clic su <strong> script e strumenti di gestione IIS </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servizi ruolo server Web</p></td>
<td align="left"><p><strong>Caratteristiche HTTP comuni:</strong></p>
<ul>
<li><p>Contenuto statico</p></li>
<li><p>Documento predefinito</p></li>
</ul>
<p><strong>Sviluppo di applicazioni:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Estensibilità .NET</p></li>
<li><p>Estensioni ISAPI</p></li>
<li><p>Filtri ISAPI</p></li>
</ul>
<p><strong>Sicurezza</strong></p>
<ul>
<li><p>Autenticazione di Windows</p></li>
<li><p>Filtro delle richieste</p></li>
</ul>
<p><strong>Strumenti di gestione:</strong></p>
<ul>
<li><p>Console di gestione di IIS</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Posizione di installazione predefinita</p></td>
<td align="left"><p>%Programmi%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL del servizio di gestione</p></td>
<td align="left"><p>URL del servizio di gestione App-V. Questa è la porta con cui comunica il server di pubblicazione.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Architettura di installazione</th>
<th align="left">Formato da usare per l'URL</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Server di gestione e server di pubblicazione sono installati nello stesso server</p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Server di gestione e server di pubblicazione installati in server diversi</p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome sito Web del servizio di pubblicazione</p></td>
<td align="left"><p>Nome per il sito Web di pubblicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Binding della porta del servizio di pubblicazione</p></td>
<td align="left"><p>Numero di porta univoco per il servizio di pubblicazione. Questa porta non può essere usata da un altro processo nel computer.</p></td>
</tr>
</tbody>
</table>



### Software per i prerequisiti di Reporting Server

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti e impostazioni obbligatorie</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Versione supportata di SQL Server</p></td>
<td align="left"><p>Per le versioni supportate, vedere <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurazioni supportate in App-V 5,1 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacchetti ridistribuibili di Visual C++ per Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>registrazione ASP.NET di 64 bit</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ruolo di Windows Server Web Server</p></td>
<td align="left"><p>Questo ruolo deve essere aggiunto a un sistema operativo server supportato per il server di gestione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Strumenti di gestione di Web Server (IIS)</p></td>
<td align="left"><p>Fare clic su <strong> script e strumenti di gestione IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Servizi ruolo server Web</p></td>
<td align="left"><p>Per ridurre il rischio di invio di dati indesiderati o malintenzionati al server di report, è necessario limitare l'accesso al servizio Web Reporting per i criteri di sicurezza aziendali.</p>
<p><strong>Caratteristiche HTTP comuni:</strong></p>
<ul>
<li><p>Contenuto statico</p></li>
<li><p>Documento predefinito</p></li>
</ul>
<p><strong>Sviluppo di applicazioni:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Estensibilità .NET</p></li>
<li><p>Estensioni ISAPI</p></li>
<li><p>Filtri ISAPI</p></li>
</ul>
<p><strong>Sicurezza</strong></p>
<ul>
<li><p>Autenticazione di Windows</p></li>
<li><p>Filtro delle richieste</p></li>
</ul>
<p><strong>Strumenti di gestione:</strong></p>
<ul>
<li><p>Console di gestione di IIS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Posizione di installazione predefinita</p></td>
<td align="left"><p>%Programmi%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome del sito Web del servizio Reporting</p></td>
<td align="left"><p>Nome del sito Web per la creazione di report.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Binding della porta del servizio Reporting</p></td>
<td align="left"><p>Numero di porta univoco per il servizio Reporting. Questa porta non può essere usata da un altro processo nel computer.</p></td>
</tr>
</tbody>
</table>



### Software per la creazione di un database

Il database delle relazioni è obbligatorio solo se si usa il server di report App-V 5,1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti e impostazioni obbligatorie</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacchetti ridistribuibili di Visual C++ per Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Posizione di installazione predefinita</p></td>
<td align="left"><p>%Programmi%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome istanza di SQL Server personalizzata (se applicabile)</p></td>
<td align="left"><p>Formato da usare: <strong> InstanceName</strong></p>
<p>Questo formato si basa sul presupposto che l'installazione si trovi nel computer locale.</p>
<p>Se specifichi il nome con il formato <strong> SVR\INSTANCE </strong> , l'installazione non riuscirà.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome database personalizzato (se applicabile)</p></td>
<td align="left"><p>Nome database univoco.</p>
<p>Impostazione predefinita: AppVReporting</p></td>
</tr>
<tr class="even">
<td align="left"><p>Posizione del server di report</p></td>
<td align="left"><p>Account del computer in cui è distribuito il server di report.</p>
<p>Formato da usare: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Amministratore dell'installazione di Reporting Server</p></td>
<td align="left"><p>Account usato per installare il server di report.</p>
<p>Formato da usare: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servizio Microsoft SQL Server e agente di servizio Microsoft SQL Server</p></td>
<td align="left"><p>Configurare i servizi da associare agli account utente che hanno accesso a query AD DS.</p></td>
</tr>
</tbody>
</table>



## Software per prerequisiti client App-V


Installare il software di prerequisito seguente per il client App-V.

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
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>L'installazione di PowerShell 3,0 richiede un riavvio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Si applica solo a Windows 7: scaricare e installare la Knowledge.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacchetti ridistribuibili di Visual C++ per Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Software prerequisito client Servizi Desktop remoto


Installare il software prerequisito seguente per il client Servizi Desktop remoto App-V.

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
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>L'installazione di PowerShell 3,0 richiede un riavvio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Si applica solo a Windows 7: scaricare e installare la Knowledge.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacchetti ridistribuibili di Visual C++ per Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Software per prerequisiti sequenziatore


**Informazioni utili prima di installare i prerequisiti:**

-   Procedura consigliata: il computer che esegue il Sequencer deve avere le stesse configurazioni hardware e software dei computer in cui vengono eseguite le applicazioni virtuali.

-   Il processo di sequenziazione è intensivo delle risorse, quindi assicurati che il computer che esegue il sequencer abbia abbondanza di memoria, un processore veloce e un disco rigido veloce. I requisiti di sistema delle applicazioni installate localmente non possono superare quelli del sequencer. Per altre informazioni, Vedi [configurazioni supportate in App-V 5,1](app-v-51-supported-configurations.md).

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
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>L'installazione di PowerShell 3,0 richiede un riavvio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Si applica solo a Windows 7: scaricare e installare la Knowledge.</p></td>
</tr>
</tbody>
</table>








## Argomenti correlati


[Pianificazione di App-V 5.1](planning-for-app-v-51.md)

[Configurazioni supportate di App-V 5.1](app-v-51-supported-configurations.md)









