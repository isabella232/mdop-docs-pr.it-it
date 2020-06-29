---
title: Informazioni su App-V 5.0 SP3
description: Informazioni su App-V 5.0 SP3
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814975"
---
# Informazioni su App-V 5.0 SP3


Usare le sezioni seguenti per esaminare le informazioni sulle modifiche significative che si applicano a Microsoft Application Virtualization (App-V) 5,0 SP3:

-   [Prerequisiti software App-V 5,0 SP3 e configurazioni supportate](#bkmk-sp3-prereq-configs)

-   [Migrazione a App-V 5,0 SP3](#bkmk-migrate-to-50sp3)

-   [Il file XML del gruppo di connessioni creato manualmente richiede l'aggiornamento allo schema](#bkmk-update-schema-cg)

-   [Miglioramenti apportati ai gruppi di connessioni](#bkmk-cg-improvements)

-   [Gli amministratori possono pubblicare e annullare la pubblicazione di pacchetti per un utente specifico](#bkmk-usersid-pub-pkgs-specf-user)

-   [Consentire solo agli amministratori di pubblicare e annullare la pubblicazione di pacchetti](#bkmk-admins-only-pub-unpub-pkgs)

-   [La chiave del registro di sistema RunVirtual supporta i pacchetti pubblicati per l'utente](#bkmk-runvirtual-reg-key)

-   [Guida di nuovi cmdlet di PowerShell e cmdlet aggiornabile](#bkmk-posh-cmdlets-help)

-   [La directory delle applicazioni virtuali primarie (PVAD) è nascosta ma può essere attivata](#bkmk-pvad-hidden)

-   [ClientVersion è necessario per visualizzare i metadati di pubblicazione di App-V](#bkmk-pub-metadata-clientversion)

-   [I registri eventi App-V sono stati consolidati](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a>Prerequisiti software App-V 5,0 SP3 e configurazioni supportate


Vedere i collegamenti seguenti per i prerequisiti software App-V 5,0 SP3 e le configurazioni supportate.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Collegamenti ai prerequisiti e alle configurazioni supportate</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)">Prerequisiti di App-V 5.0 SP3</a></p></td>
<td align="left"><p>Software prerequisito che è necessario installare prima di avviare l'installazione di App-V 5,0 SP3</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">Configurazioni supportate da App-V 5.0 SP3</a></p></td>
<td align="left"><p>Requisiti hardware e sistemi operativi supportati per i componenti App-V Server, sequencer e client</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a>Migrazione a App-V 5,0 SP3


Usare le informazioni seguenti per eseguire l'aggiornamento a App-V 5,0 SP3 da versioni precedenti.

### Prima di iniziare l'aggiornamento

Prima di iniziare l'aggiornamento, esaminare le informazioni seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elementi da rivedere prima dell'aggiornamento</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Componenti da aggiornare</p></td>
<td align="left"><ol>
<li><p>App-V Server</p></li>
<li><p>Sequencer</p></li>
<li><p>App-V client o client RDS (Remote Desktop Services) App-V</p></li>
<li><p>Gruppi di connessioni</p></li>
</ol>
<div class="alert">
<strong>Nota</strong><br/><p>Per usare l'interfaccia utente del client App-V, Scarica la versione esistente dall' <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> applicazione Microsoft Application Virtualization 5,0 client </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Aggiornamento da App-V 4. x</p></td>
<td align="left"><p>Devi prima eseguire l'aggiornamento a App-V 5,0. Non è possibile eseguire l'aggiornamento direttamente da App-V 4. x a App-V 5,0 SP3.</p>
<p>Per altre informazioni, vedi:</p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">Informazioni su App-V 5.0</a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">Pianificazione per la migrazione da una versione precedente di App-V</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aggiornamento da App-V 5,0 o versione successiva</p></td>
<td align="left"><p>È possibile eseguire l'aggiornamento a App-V 5,0 SP3 direttamente da una delle versioni seguenti:</p>
<ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul>
<p>Per eseguire l'aggiornamento a App-V 5,0 SP3, seguire la procedura descritta nelle sezioni rimanenti di questo articolo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modifiche necessarie ai pacchetti e ai gruppi di connessioni dopo l'aggiornamento</p></td>
<td align="left"><p>Nessuna. I pacchetti e i gruppi di connessioni continueranno a funzionare al momento.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>Procedura per aggiornare l'infrastruttura di App-V

Completare i passaggi seguenti per aggiornare ogni componente dell'infrastruttura App-V in App-V 5,0 SP3.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Per altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Passaggio 1: aggiornare l'App-V Server.</p>
<p>Se non si usa App-V Server, ignorare questo passaggio e passare al passaggio successivo.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Il client App-V 5,0 SP3 è compatibile con il server App-V 5,0 SP1.</p>
</div>
<div>

</div></td>
<td align="left"><p>Segui questa procedura: </p>
<ol>
<li><p>Esaminare le <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> Note sulla versione per App-v 5,0 SP3 </a> per problemi che possono influire sull'installazione di App-v Server.</p></li>
<li><p>Eseguire una delle operazioni seguenti, a seconda del metodo usato per aggiornare il database di gestione e/o il database di report:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo di aggiornamento del database</th>
<th align="left">Passaggio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>Ignorare questo passaggio e passare al passaggio 3, "Se si esegue l'aggiornamento del server App-V..."</p></td>
</tr>
<tr class="even">
<td align="left"><p>Script SQL</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Database di gestione</strong></p></td>
<td align="left"><p>Per installare o aggiornare, vedere <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> gli script SQL per installare o aggiornare il database del server di gestione di App-V 5,0 SP3 Fail </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Database di report</strong></p></td>
<td align="left"><p>Seguire i passaggi descritti in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> come distribuire i database di App-V tramite gli script SQL </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p>Se si sta aggiornando il pacchetto di hotfix App-v 5,0 SP1 3 o versione successiva, eseguire la procedura descritta nella sezione <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> controllare le chiavi del registro di sistema dopo l'installazione del server App-v 5,0 SP3 </a> .</p></li>
<li><p>Seguire la procedura descritta in <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> come distribuire il server App-V 5,0 </a> .</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Passaggio 2: aggiornare l'App-V Sequencer.</p></td>
<td align="left"><p>Vedere <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> come installare il sequencer </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Passaggio 3: aggiornare il client App-V o client RDS App-v.</p></td>
<td align="left"><p>Scopri <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> come distribuire il client App-V </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a>Controllare le chiavi del registro di sistema prima di installare il server App-V 5,0 SP3

Questo è il passaggio 3 della tabella precedente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Quando è necessario eseguire questo passaggio</strong></p></td>
<td align="left"><p>Si esegue l'aggiornamento da App-V SP1 con tutti i pacchetti di hotfix successivi installati usando un file msp.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Quali componenti richiedono di eseguire questo passaggio</strong></p></td>
<td align="left"><p>Solo i componenti di App-V Server che si stanno aggiornando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Quando è necessario eseguire questo passaggio</strong></p></td>
<td align="left"><p>Prima di aggiornare l'App-V Server a App-V 5,0 SP3</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Cosa è necessario fare</strong></p></td>
<td align="left"><p>Usando le informazioni nelle tabelle seguenti, aggiornare ogni valore della chiave del registro <code>HKLM\Software\Microsoft\AppV\Server</code> di sistema in con il valore specificato nell'installazione del server originale. Il completamento di questo passaggio ripristina i valori del registro di sistema che potrebbero essere stati rimossi quando sono stati installati i pacchetti di hotfix di App-V SP1.</p></td>
</tr>
</tbody>
</table>



**Tasto ManagementDatabase**

Se si sta installando il database di gestione, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome chiave</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Descrive se è necessario un account di accesso pubblico per accedere ai database di gestione non locali. Il valore è impostato su "1" se necessario.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_NAME</p></td>
<td align="left"><p>Nome del database di gestione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Account usato per l'accesso in lettura (pubblico) al database di gestione.</p>
<p>Usato quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificatore sicuro (SID) dell'account usato per l'accesso in lettura (pubblico) al database di gestione.</p>
<p>Usato quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Istanza di SQL Server per il database di gestione.</p>
<p>Se il valore è vuoto, viene usata l'istanza di database predefinita.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Account usato per l'accesso in scrittura (amministratore) al database di gestione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificatore sicuro (SID) dell'account usato per l'accesso in scrittura (amministratore) al database di gestione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Account del computer remoto di Management Server (dominio\account).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Account di accesso dell'amministratore dell'installazione per il server di gestione (dominio\account).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Valori validi:</p>
<ul>
<li><p><strong>1 </strong> -il servizio di gestione si trova nel computer locale, ovvero MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT è vuoto.</p></li>
<li><p><strong>0 </strong> - il servizio di gestione si trova in un computer diverso dal computer locale.</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Tasto ManagementService**

Se si sta installando il server di gestione, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ManagementService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome chiave</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MANAGEMENT_ADMINACCOUNT</p></td>
<td align="left"><p>Gruppo o account Active Directory Domain Services (AD DS) autorizzato a gestire App-V (dominio\account).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Istanza di SQL Server che contiene il database di gestione.</p>
<p>Se il valore è vuoto, viene usata l'istanza di database predefinita.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Nome del server SQL remoto con il database di gestione.</p>
<p>Se il valore è vuoto, viene usato il computer locale.</p></td>
</tr>
</tbody>
</table>



**Tasto ReportingDatabase**

Se si sta installando il database delle relazioni, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome chiave</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Descrive se è necessario un account di accesso pubblico per accedere a database di report non locali. Il valore è impostato su "1" se necessario.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_NAME</p></td>
<td align="left"><p>Nome del database di report.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Account usato per l'accesso in lettura (pubblico) al database di report.</p>
<p>Usato quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificatore sicuro (SID) dell'account usato per l'accesso in lettura (pubblico) al database di report.</p>
<p>Usato quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Istanza di SQL Server per il database di report.</p>
<p>Se il valore è vuoto, viene usata l'istanza di database predefinita.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Account del computer remoto di Reporting Server (dominio\account).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Account di accesso dell'amministratore dell'installazione per il server di report (dominio\account).</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Valori validi:</p>
<ul>
<li><p><strong>1 </strong> -il servizio Reporting si trova nel computer locale, ovvero REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT è vuoto.</p></li>
<li><p><strong>0 </strong> - il servizio Reporting si trova in un computer diverso dal computer locale.</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Tasto ReportingService**

Se si sta installando il server di Reporting, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ReportingService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome chiave</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Istanza di SQL Server per il database di report.</p>
<p>Se il valore è vuoto, viene usata l'istanza di database predefinita.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Nome del server SQL remoto con il database di report.</p>
<p>Se il valore è vuoto, viene usato il computer locale.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-update-schema-cg"></a>Il file XML del gruppo di connessioni creato manualmente richiede l'aggiornamento allo schema


Se si crea manualmente il file XML del gruppo di connessioni e si vogliono usare le nuove funzionalità "pacchetti facoltativi" e "Usa qualsiasi versione" descritte in [miglioramenti ai gruppi di connessioni](#bkmk-cg-improvements), è necessario specificare lo schema seguente nel file XML:

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

Per esempi e altre informazioni, vedere [informazioni sul file del gruppo di connessioni](about-the-connection-group-file.md).

## <a href="" id="bkmk-cg-improvements"></a>Miglioramenti apportati ai gruppi di connessioni


Puoi gestire i gruppi di connessioni più facilmente usando pacchetti facoltativi e altri miglioramenti che sono stati aggiunti in App-V 5,0 SP3. Nella tabella seguente sono riepilogate le attività che è possibile eseguire con le nuove caratteristiche dei gruppi di connessioni e i collegamenti a informazioni più dettagliate su ogni attività.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività/funzionalità</th>
<th align="left">Descrizione</th>
<th align="left">Collegamenti ad altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Abilitare un gruppo di connessioni per includere pacchetti facoltativi</p></td>
<td align="left"><p>L'inclusione di pacchetti facoltativi in un gruppo di connessioni consente di determinare in modo dinamico quali applicazioni verranno incluse nell'ambiente virtuale del gruppo di connessioni, in base alle applicazioni a cui gli utenti hanno diritto.</p>
<p>Non è necessario gestire il numero di gruppi di connessioni perché è possibile combinare pacchetti facoltativi e non facoltativi nello stesso gruppo di connessioni. La combinazione di pacchetti consente a diversi gruppi di utenti di usare lo stesso gruppo di connessioni, anche se gli utenti potrebbero avere un solo pacchetto in comune.</p>
<p><strong>Esempio </strong> : è possibile abilitare un pacchetto con Microsoft Office per tutti gli utenti, ma abilitare diversi pacchetti facoltativi, che contengono diversi plug-in di Office, per i diversi sottoinsiemi di utenti.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">Come usare i pacchetti facoltativi nei gruppi di connessione</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Annullare la pubblicazione o eliminare un pacchetto facoltativo senza modificare il gruppo di connessioni</p></td>
<td align="left"><p>Annullare la pubblicazione o eliminare o annullare la pubblicazione e pubblicare di nuovo un pacchetto facoltativo, che si trova in un gruppo di connessioni, senza dover disabilitare o riabilitare il gruppo di connessioni nel client App-V.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">Come usare i pacchetti facoltativi nei gruppi di connessione</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pubblicare i gruppi di connessioni che contengono i pacchetti pubblicati dall'utente e pubblicati globalmente</p></td>
<td align="left"><p>Creare un gruppo di connessioni pubblicato dall'utente che contiene i pacchetti pubblicati dall'utente e pubblicati globalmente.</p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)">Come creare un gruppo di connessione con pacchetti pubblicati dall'utente e pubblicati globalmente</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Creare un gruppo di connessioni ignorare la versione del pacchetto</p></td>
<td align="left"><p>Configurare un gruppo di connessioni per accettare qualsiasi versione di un pacchetto, che consente di aggiornare un pacchetto senza dover disabilitare il gruppo di connessioni. Inoltre, se c'è un pacchetto facoltativo con una versione non corretta nel gruppo di connessioni, il pacchetto viene ignorato e non bloccherà l'ambiente virtuale del gruppo di connessioni da creare.</p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)">Come impostare un gruppo di connessione in modo che ignori la versione del pacchetto</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Limitare le funzionalità di pubblicazione degli utenti finali</p></td>
<td align="left"><p>Consente solo agli amministratori (non agli utenti finali) di pubblicare pacchetti e di abilitare i gruppi di connessioni.</p></td>
<td align="left"><p>Per informazioni sui gruppi di connessioni, vedere <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> come consentire solo agli amministratori di abilitare i gruppi di connessioni</a></p>
<p>Per informazioni sui pacchetti, vedere gli articoli seguenti:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo</th>
<th align="left">Collegamento ad altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Console di gestione</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)">Come pubblicare un pacchetto tramite la console di gestione</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)">Come gestire i gruppi di connessione in un computer autonomo con PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sistema di distribuzione elettronica software di terze parti</p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)">Come consentire solo agli amministratori di pubblicare i pacchetti con ESD</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>Abilitare o disabilitare un gruppo di connessioni per un utente specifico</p></td>
<td align="left"><p>Gli amministratori possono abilitare o disabilitare un gruppo di connessioni per un utente specifico usando il <strong> parametro facoltativo-UserSID </strong> con i cmdlet seguenti:</p>
<ul>
<li><p>Enable-AppVClientConnectionGroup</p></li>
<li><p>Disable-AppVClientConnectionGroup</p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)">Come gestire i gruppi di connessione in un computer autonomo con PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unione di percorsi di pacchetto identici in una directory virtuale in gruppi di connessioni</p></td>
<td align="left"><p>Se due o più pacchetti in un gruppo di connessioni contengono percorsi di directory identici, i percorsi vengono uniti in un'unica directory virtuale all'interno dell'ambiente virtuale del gruppo di connessioni.</p>
<p>Questa unione di percorsi consente a un'applicazione in un pacchetto di accedere ai file che si trovano in un pacchetto diverso.</p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)">Informazioni sull'ambiente virtuale del gruppo di connessione</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a>Gli amministratori possono pubblicare e annullare la pubblicazione di pacchetti per un utente specifico


Gli amministratori possono usare i cmdlet seguenti per pubblicare o annullare la pubblicazione di pacchetti per un utente specifico. Per usare i cmdlet, immettere il parametro **– UserSID** , seguito dall'identificatore di sicurezza dell'utente (SID). Per altre informazioni, vedi:

-   [Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cmdlet</th>
<th align="left">Esempi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Publish-AppvClientPackage</p></td>
<td align="left"><p>Publish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
<tr class="even">
<td align="left"><p>Annulla pubblicazione-AppvClientPackage</p></td>
<td align="left"><p>UNPUBLISH-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a>Consentire solo agli amministratori di pubblicare e annullare la pubblicazione di pacchetti


È possibile abilitare solo gli amministratori (non gli utenti finali) a pubblicare e annullare la pubblicazione di pacchetti usando uno dei metodi seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Impostazione di Criteri di gruppo</p></td>
<td align="left"><p>Passare al nodo oggetto Criteri di gruppo seguente:</p>
<p><strong>Criteri di configurazione del computer &gt; &gt; modelli amministrativi &gt; &gt; App-V &gt; Publishing </strong> .</p>
<p>Abilitare l' <strong> impostazione Richiedi i criteri di gruppo pubblica come amministratore </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)">Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a>La chiave del registro di sistema RunVirtual supporta i pacchetti pubblicati per l'utente


App-V 5,0 SP3 aggiunge il supporto per l'uso della chiave del registro di sistema **RunVirtual** con le applicazioni virtualizzate presenti nei pacchetti pubblicati dall'utente. La chiave del registro di sistema **RunVirtual** consente di eseguire un'applicazione installata localmente in un ambiente virtuale, insieme alle applicazioni virtualizzate tramite App-V.

In precedenza, le applicazioni virtualizzate nei pacchetti App-V dovevano essere pubblicate globalmente. Per altre informazioni su **RunVirtual** e su altri metodi di gestione delle applicazioni installate localmente in un ambiente virtuale con applicazioni virtualizzate, vedere [eseguire un'applicazione installata localmente in un ambiente virtuale con applicazioni virtualizzate](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).

## <a href="" id="bkmk-posh-cmdlets-help"></a>Guida di nuovi cmdlet di PowerShell e cmdlet aggiornabile


I nuovi cmdlet di PowerShell e la guida per i cmdlet aggiornabili sono inclusi in App-V 5,0 SP3. Per scaricare i moduli cmdlet, vedere [come caricare i cmdlet di PowerShell e ottenere la guida per i cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).

### Nuovi cmdlet di PowerShell per server App-V 5,0 SP3

Sono stati aggiunti nuovi cmdlet di Windows PowerShell per App-V Server per gestire i gruppi di connessioni.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cmdlet</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Add-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Accoda un pacchetto alla fine di un gruppo di connessioni&#39;elenco di pacchetti s e consente di configurare il pacchetto come facoltativo e/o senza una versione all'interno del gruppo di connessioni.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Set-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Consente di modificare i dettagli del pacchetto del gruppo di connessioni, ad esempio se è facoltativo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Remove-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Rimuove un pacchetto da un gruppo di connessioni.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a>Ottenere assistenza per i cmdlet di PowerShell

La guida per i cmdlet è disponibile nei formati seguenti:

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
<td align="left"><p>Per ottenere la guida più recente dopo il download del modulo cmdlet:</p>
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
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>In TechNet come pagine Web</p></td>
<td align="left"><p>Vedere il nodo App-V in <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automazione di Microsoft Desktop Optimization Pack con Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>



Per altre informazioni, vedere [come caricare i cmdlet di PowerShell e ottenere la guida per i cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).

## <a href="" id="bkmk-pvad-hidden"></a>La directory delle applicazioni virtuali primarie (PVAD) è nascosta ma può essere attivata


La directory delle applicazioni virtuali primarie (PVAD) è nascosta in App-V 5,0 SP3, ma è possibile riattivarla e renderla visibile usando uno dei metodi seguenti:

<table>
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
<td align="left"><p>Usare un parametro della riga di comando</p></td>
<td align="left"><p>Passare il <strong> parametro – EnablePVADControl </strong> al <strong>Sequencer.exe</strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Creare una sottochiave del registro di sistema</p></td>
<td align="left"><ol>
<li><p>Nell'editor del registro di sistema passare a: <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong>Nota</strong><br/><p>Se la <code>Compatibility</code> sottochiave non esiste, è necessario crearla.</p>
</div>
<div>

</div></li>
<li><p>Crea un valore DWORD denominato <strong> EnablePVADControl </strong> e imposta il valore su <strong> 1 </strong> .</p>
<p>Un valore pari a <strong> 0 </strong> indica che PVAD è nascosto.</p></li>
</ol></td>
</tr>
</tbody>
</table>



**Altre informazioni su PVAD:** Quando si usa sequencer per creare un pacchetto, è possibile immettere qualsiasi percorso di installazione per il pacchetto. Nelle versioni precedenti di App-V era necessario specificare la directory dell'applicazione virtuale primaria (PVAD) dell'applicazione come percorso. PVAD è la directory in cui in genere si installa un'applicazione nel computer locale se non si usa l'App-V. Ad esempio, se si sta installando Office in un computer, il PVAD in genere sarebbe C:\\Programmi \\Programmi\\microsoft Office\\.

## <a href="" id="bkmk-pub-metadata-clientversion"></a>ClientVersion è necessario per visualizzare i metadati di pubblicazione di App-V


In App-V 5,0 SP3 è necessario specificare i valori seguenti nell'indirizzo quando si esegue una query sul server di pubblicazione App-V per i metadati:

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
<td align="left"><p>Se si omette il <strong> </strong> parametro ClientVersion dalla query, i metadati escludono le nuove funzionalità App-V 5,0 SP3.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Clientos</strong></p></td>
<td align="left"><p>È necessario specificare questo valore solo se si selezionano sistemi operativi client specifici quando si sequenzia il pacchetto. Se si seleziona l'impostazione predefinita (tutti i sistemi operativi), non specificare questo valore nella query.</p>
<p>Se si omette il <strong> parametro clientos </strong> dalla query, solo i pacchetti sequenziati per supportare qualsiasi sistema operativo verranno visualizzati nei metadati.</p></td>
</tr>
</tbody>
</table>



Per la sintassi e gli esempi di questa query, vedere [visualizzazione dei metadati di pubblicazione di App-V Server](viewing-app-v-server-publishing-metadata.md).

## <a href="" id="bkmk-event-logs-moved"></a>I registri eventi App-V sono stati consolidati


I registri eventi seguenti, precedentemente presenti nei **registri delle applicazioni e dei servizi/Microsoft/appv/ &lt; app- &gt; V Component**, sono stati spostati in **registri applicazioni e servizi/Microsoft/appv/ServiceLog**.

Per visualizzare i registri, selezionare Visualizza **Mostra** i &gt; **registri analitici e di debug** nell'applicazione Visualizzatore eventi.

Client per il catalogo client-client di integrazione-client di orchestrazione-client di PackageConfig-client di scripting-client di servizi-Vemgr client-VFSC FilesystemMetadataLibrary ManifestLibrary sottosistemi PolicyLibrary-sottosistemi ActiveX-sottosistemi di sistema-sottosistemi-com-FTA

## Come ottenere le tecnologie MDOP


App-V fa parte di Microsoft Desktop Optimization Pack (MDOP). MDOP fa parte di Microsoft Software Assurance. Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).






## Argomenti correlati


[Note sulla versione di App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)









