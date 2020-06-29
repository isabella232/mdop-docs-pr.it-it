---
title: Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager
description: Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825996"
---
# Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager


Prima di avviare l'installazione di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker, è necessario completare i prerequisiti elencati in questo argomento. Questi prerequisiti si applicano alla topologia MBAM autonoma e all'integrazione di System Center Configuration Manager.

Se si sta distribuendo MBAM con System Center Configuration Manager, è necessario completare i prerequisiti aggiuntivi, elencati nei [prerequisiti del server mbam 2,5 che si applicano solo alla topologia di integrazione di Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).

Per un elenco dei sistemi operativi e hardware supportati per MBAM, Vedi le [configurazioni supportate di mbam 2,5](mbam-25-supported-configurations.md).

**Importante**  
Se BitLocker è stato usato senza MBAM, è necessario decrittografare l'unità e quindi cancellare TPM usando TPM. msc. MBAM non può assumere la proprietà del TPM se il PC client è già crittografato e la password del proprietario del TPM è stata creata.



## Ruoli e account di MBAM necessari


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
<td align="left"><p>Gruppi creati in servizi di dominio Active Directory (AD DS)</p></td>
<td align="left"><p>Vedere <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> pianificazione per i gruppi e gli account di MBAM 2,5 </a> per una descrizione di questi gruppi e account.</p></td>
</tr>
</tbody>
</table>



## Prerequisiti per il database di ripristino


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
<td align="left"><p>Versione supportata di SQL Server</p></td>
<td align="left"><p>Installare Microsoft SQL Server con le regole di confronto SQL_Latin1_General_CP1_CI_AS.</p>
<p>Vedi <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> MBAM 2,5 configurazioni supportate </a> per le versioni supportate.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Autorizzazioni di SQL Server obbligatorie</p></td>
<td align="left"><p>Autorizzazioni necessarie:</p>
<ul>
<li><p>Ruoli del server di accesso istanza di SQL Server:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>Diritti di istanza di SQL Server Reporting Services:</p>
<ul>
<li><p>Creare cartelle</p></li>
<li><p>Pubblicare report</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Facoltativo: installare la funzionalità di crittografia dati trasparente (Transparent Data Encryption) disponibile in SQL Server</p></td>
<td align="left"><p>La funzionalità SQL Server di transcription esegue la crittografia di I/O in tempo reale e la decrittografia dei file di dati e di log, che possono aiutarti a rispettare leggi, normative e linee guida applicabili a vari settori.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Transparent esegue la decrittografia in tempo reale delle informazioni sul database. Questo significa che, se si stanno visualizzando le informazioni chiave di ripristino nel database di SQL Server e si è connessi con un account che dispone delle autorizzazioni per il database, le informazioni sulla chiave di ripristino sono visibili. Per saperne di più su Transparent, vedere <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considerazioni sulla sicurezza di MBAM 2,5 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Servizi motore di database di SQL Server</p></td>
<td align="left"><p>I servizi motore di database di SQL Server devono essere installati e eseguiti durante l'installazione di MBAM server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 o versione successiva</p></td>
<td align="left"><p>Windows PowerShell non deve essere installato nel server di database di ripristino se si usa Windows PowerShell per configurare il database da un computer remoto.</p></td>
</tr>
</tbody>
</table>



## Prerequisiti per il database di conformità e controllo


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
<td align="left"><p>Versione supportata di SQL Server</p></td>
<td align="left"><p>Installare SQL Server con le regole di confronto SQL_Latin1_General_CP1_CI_AS.</p>
<p>Vedi <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> MBAM 2,5 configurazioni supportate </a> per le versioni supportate.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Autorizzazioni di SQL Server obbligatorie</p></td>
<td align="left"><p>Autorizzazioni necessarie:</p>
<ul>
<li><p>Ruoli del server di accesso istanza di SQL Server:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>Diritti di istanza di SQL Server Reporting Services:</p>
<ul>
<li><p>Creare cartelle</p></li>
<li><p>Pubblicare report</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Facoltativo: installare la funzionalità di crittografia dei dati trasparente (Transparent Data Encryption) in SQL Server</p></td>
<td align="left"><p>La funzionalità SQL Server di transcription esegue la crittografia di I/O in tempo reale e la decrittografia dei file di dati e di log, che possono aiutarti a rispettare leggi, normative e linee guida applicabili a vari settori.</p>
<p>Transparent esegue la decrittografia in tempo reale delle informazioni sul database. Questo significa che, se si stanno visualizzando le informazioni chiave di ripristino nel database di SQL Server e si è connessi con un account che dispone delle autorizzazioni per il database, le informazioni sulla chiave di ripristino sono visibili. Per saperne di più su Transparent, vedere <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considerazioni sulla sicurezza di MBAM 2,5 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servizi motore di database di SQL Server</p></td>
<td align="left"><p>I servizi motore di database di SQL Server devono essere installati e eseguiti durante l'installazione di MBAM server. Tuttavia, SQL Server può essere eseguito in remoto; non deve essere nello stesso server in cui si sta installando il software del server MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 o versione successiva</p></td>
<td align="left"><p>Windows PowerShell non deve essere installato nel server di database di conformità e controllo se si usa Windows PowerShell per configurare il database da un computer remoto.</p></td>
</tr>
</tbody>
</table>



## Prerequisiti per i report


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
<td align="left"><p>Versione supportata di SQL Server</p></td>
<td align="left"><p>Installare SQL Server con le regole di confronto SQL_Latin1_General_CP1_CI_AS.</p>
<p>Vedi <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> MBAM 2,5 configurazioni supportate </a> per le versioni supportate.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p>SSRS deve essere installato ed eseguito durante l'installazione di MBAM server.</p>
<p>Configurare SSRS in &quot; &quot; modalità nativa e non in modalità non configurata o &quot; SharePoint &quot; .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Diritti delle istanze di SSRS: necessari per la configurazione dei report solo se si installano database in un server separato dal server in cui sono configurati i report.</p></td>
<td align="left"><p>Diritti di istanza obbligatori:</p>
<ul>
<li><p>Creare cartelle</p></li>
<li><p>Pubblicare report</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows PowerShell 3,0 o versione successiva</p></td>
<td align="left"><p>Windows PowerShell non deve essere installato in questo server di database se si usa Windows PowerShell per configurare il database da un computer remoto.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a>Prerequisiti per l'amministrazione e il server di monitoraggio


La tabella seguente elenca i prerequisiti di installazione per l'amministrazione e il server di monitoraggio di MBAM.

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
<td align="left"><p>Ruolo di Windows Server Web Server</p></td>
<td align="left"><p>Questo ruolo deve essere aggiunto a un sistema operativo server supportato per la funzionalità di amministrazione e monitoraggio Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Strumenti di gestione di Web Server (IIS)</p></td>
<td align="left"><p>Fare clic su <strong> script e strumenti di gestione IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Certificato SSL</strong></p></td>
<td align="left"><p>Facoltativo. Per proteggere le comunicazioni tra i computer client e i servizi Web, è necessario ottenere e installare un certificato firmato da un'autorità di sicurezza attendibile.</p></td>
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
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Caratteristiche di Windows Server</p></td>
<td align="left"><p><strong>Caratteristiche di .NET Framework 4,5:</strong></p>
<ul>
<li><p><strong>.NET Framework 4,5 o 4,6</strong></p>
<ul>
<li><p><strong>Windows Server 2016 </strong> - .net Framework 4,6 è già installato per queste versioni di Windows Server, ma è necessario abilitarlo.</p></li>  
<li><p><strong>Windows Server 2012 o Windows Server 2012 R2 </strong> - .net Framework 4,5 è già installato per queste versioni di Windows Server, ma è necessario abilitarlo.</p></li>
<li><p><strong>Windows Server 2008 R2 </strong> - .net Framework 4,5 non è incluso in windows Server 2008 R2, quindi è necessario <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> scaricare Microsoft .NET Framework 4,5 </a> e installarlo separatamente.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se si esegue l'aggiornamento da MBAM 2,0 o MBAM 2,0 SP1 e si vuole installare .NET Framework 4,5, vedere <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> Note sulla versione per mbam 2,5 </a> per un ulteriore passaggio necessario per far funzionare i siti Web.</p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong>Attivazione di WCF</strong></p>
<ul>
<li><p>Attivazione HTTP</p></li>
<li><p>Attivazione non HTTP (solo per Windows Server 2008, 2012 e 2012 R2)</p>
<p></p></li>
</ul></li>
<li><p><strong>Attivazione TCP</strong></p></li>
</ul>
<p><strong>Servizio Attivazione processo Windows:</strong></p>
<ul>
<li><p>Modello di processo</p></li>
<li><p>Ambiente .NET Framework</p></li>
<li><p>API di configurazione</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">ASP.NET MVC 4 download</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome dell'entità servizio (SPN)</p></td>
<td align="left"><p>Le applicazioni Web richiedono un SPN per il nome host virtuale sotto l'account di dominio usato per i pool di applicazioni Web.</p>
<p>Se i diritti amministrativi consentono di creare nomi SPN in servizi di dominio Active Directory, MBAM crea l'SPN per l'utente. <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> </a> Per informazioni sui diritti necessari per la creazione di nomi SPN, vedere Setspn.</p>
<p>Se non si hanno diritti amministrativi per la creazione di nomi SPN, è necessario chiedere agli amministratori di Active Directory dell'organizzazione di creare l'SPN usando il comando seguente.</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>Nell'esempio di codice il nome host virtuale è mbamvirtual.contoso.com e l'account di dominio usato per i pool di applicazioni Web è contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se si sta configurando il bilanciamento del carico, usare lo stesso account del pool di applicazioni in tutti i server.</p>
</div>
<div>

</div>
<p>Per altre informazioni sulla registrazione di SPN per nomi host completi, NetBIOS e personalizzati, vedere <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> pianificazione di come proteggere i siti Web di mbam </a> .</p></td>
</tr>
</tbody>
</table>



## Prerequisiti per il portale self-service


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
<td align="left"><p>Versione supportata di Windows Server</p></td>
<td align="left"><p>Vedi <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> MBAM 2,5 configurazioni supportate </a> per le versioni supportate.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">ASP.NET MVC 4 download</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Strumenti di gestione di IIS per servizi Web</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome dell'entità servizio (SPN)</p></td>
<td align="left"><p>Le applicazioni Web richiedono un SPN per il nome host virtuale sotto l'account di dominio usato per i pool di applicazioni Web.</p>
<p>Se i diritti amministrativi consentono di creare nomi SPN in servizi di dominio Active Directory, MBAM crea l'SPN per l'utente. <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> </a> Per informazioni sui diritti necessari per la creazione di nomi SPN, vedere Setspn.</p>
<p>Se non si hanno diritti amministrativi per la creazione di nomi SPN, è necessario chiedere agli amministratori di Active Directory degli amministratori dell'organizzazione dell'organizzazione di creare l'SPN usando il comando seguente.</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>Nell'esempio di codice il nome host virtuale è mbamvirtual.contoso.com e l'account di dominio usato per i pool di applicazioni Web è contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se si sta configurando il bilanciamento del carico, usare lo stesso account del pool di applicazioni in tutti i server.</p>
</div>
<div>

</div>
<p>Per altre informazioni sulla registrazione di SPN per nomi host completi, NetBIOS e personalizzati, vedere <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> pianificazione di come proteggere i siti Web di mbam </a> .</p></td>
</tr>
</tbody>
</table>



## Prerequisiti per la workstation di gestione


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
<td align="left"><p>Prima di installare il client MBAM, scaricare i modelli dei criteri di gruppo di MBAM da <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> come ottenere i modelli di criteri di gruppo di MDOP </a> e configurarli con le impostazioni da implementare nella propria organizzazione per la crittografia unità BitLocker.</p></td>
<td align="left"><p>Prima di installare il client MBAM, eseguire le operazioni seguenti:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Operazione da eseguire</th>
<th align="left">Dove ottenere le istruzioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copiare i modelli dei criteri di gruppo di MBAM</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copia dei modelli dei Criteri di gruppo di MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Modificare le impostazioni dei criteri di gruppo</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Modifica delle impostazioni dei Criteri di gruppo di MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## Argomenti correlati


[Preparazione dell'ambiente per MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Pianificazione della distribuzione di MBAM 2.5](planning-to-deploy-mbam-25.md)

[Configurazioni supportate di MBAM 2.5](mbam-25-supported-configurations.md)




## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




