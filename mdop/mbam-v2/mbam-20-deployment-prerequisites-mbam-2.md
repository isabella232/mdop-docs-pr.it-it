---
title: Prerequisiti per la distribuzione di MBAM 2.0
description: Prerequisiti per la distribuzione di MBAM 2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826015"
---
# Prerequisiti per la distribuzione di MBAM 2.0


Prima di avviare l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM), è necessario assicurarsi di avere soddisfatto i prerequisiti per installare il prodotto. Questa sezione contiene informazioni utili per pianificare correttamente l'ambiente di elaborazione prima di distribuire le funzionalità e i client del server di amministrazione e monitoraggio di Microsoft BitLocker. Se si sta installando MBAM con Configuration Manager, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) per i prerequisiti aggiuntivi.

## Prerequisiti di installazione per le caratteristiche del server MBAM


Ogni funzionalità di MBAM Server include prerequisiti specifici che devono essere soddisfatti prima che le funzionalità di MBAM possano essere installate correttamente. La configurazione di MBAM controlla che tutti i prerequisiti vengano soddisfatti prima che l'installazione venga avviata.

### Prerequisiti per l'amministrazione e il server di monitoraggio

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
<td align="left"><p><strong>Ruolo di Windows Server Web Server</strong></p></td>
<td align="left"><p>Questo ruolo deve essere aggiunto a un sistema operativo server supportato per la funzionalità di amministrazione e monitoraggio Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Strumenti di gestione di Web Server (IIS)</strong></p></td>
<td align="left"><p>Selezionare <strong> script e strumenti di gestione di IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Certificato SSL</strong></p></td>
<td align="left"><p>Facoltativo. Per proteggere le comunicazioni tra i client e i servizi Web, è necessario ottenere e installare un certificato firmato da un'autorità di sicurezza attendibile.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Servizi ruolo server Web</strong></p></td>
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
<td align="left"><p><strong>Caratteristiche di Windows Server</strong></p></td>
<td align="left"><p><strong>Caratteristiche di .NET Framework 3.5.1:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>Attivazione di WCF</p>
<ul>
<li><p>Attivazione HTTP</p></li>
<li><p>Attivazione non HTTP</p></li>
</ul></li>
</ul>
<p><strong>Servizio Attivazione processo Windows:</strong></p>
<ul>
<li><p>Modello di processo</p></li>
<li><p>Ambiente .NET</p></li>
<li><p>API di configurazione</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Nota**  
Per un elenco dei sistemi operativi supportati, Vedi le [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).



### Prerequisiti per i report di conformità e controllo

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
<td align="left"><p>Versione supportata di SQL Server</p>
<p>Vedi <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> MBAM 2,0 configurazioni supportate </a> per le versioni supportate.</p></td>
<td align="left"><p>Installare SQL Server con:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS regole di confronto</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Diritti delle istanze di SSRS: necessari per l'installazione di report solo se si stanno installando database in un server separato dai report.</p></td>
<td align="left"><p>Diritti di istanza obbligatori:</p>
<ul>
<li><p>Creare cartelle</p></li>
<li><p>Pubblicare report</p></li>
</ul>
<p>SSRS deve essere installato ed eseguito durante l'installazione di MBAM server. Configurare SSRS in modalità "nativa" e non in modalità non configurata o "SharePoint".</p></td>
</tr>
</tbody>
</table>



### Prerequisiti per il database di ripristino

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
<td align="left"><p>Versione supportata di SQL Server</p>
<p>Vedi <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> MBAM 2,0 configurazioni supportate </a> per le versioni supportate.</p></td>
<td align="left"><p>Installare SQL Server con:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS regole di confronto</p></li>
<li><p>Strumenti di gestione di SQL Server</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Autorizzazioni di SQL Server obbligatorie</p></td>
<td align="left"><p>Autorizzazioni necessarie:</p>
<ul>
<li><p>Ruoli del server di accesso alle istanze SQL:</p>
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
<td align="left"><p>Funzionalità di crittografia dei dati trasparente facoltativa-install disponibile in SQL Server</p></td>
<td align="left"><p>La funzionalità SQL Server di transcription esegue la crittografia di I/O in tempo reale e la decrittografia dei file di dati e di log, che possono aiutarti a rispettare numerose leggi, normative e linee guida stabilite in diversi settori.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Transparent esegue la decrittografia in tempo reale delle informazioni sul database, il che significa che, se l'account in cui è stato effettuato l'accesso ha le autorizzazioni per il database mentre si visualizzano le informazioni chiave di ripristino nelle tabelle di SQL Server, le informazioni sulla chiave di ripristino sono visibili.</p>
</div>
<div>

</div>
<p>Altre informazioni su Transparence: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 considerazioni sulla sicurezza </a> .</p></td>
</tr>
</tbody>
</table>



### Prerequisiti per il database di conformità e controllo

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
<td align="left"><p>Versione supportata di SQL Server</p>
<p>Vedi <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> MBAM 2,0 configurazioni supportate </a> per le versioni supportate.</p></td>
<td align="left"><p>Installare SQL Server con:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS regole di confronto</p></li>
<li><p>Strumenti di gestione di SQL Server</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Autorizzazioni di SQL Server obbligatorie</p></td>
<td align="left"><p>Autorizzazioni necessarie:</p>
<ul>
<li><p>Ruoli del server di accesso alle istanze SQL:</p>
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
<td align="left"><p>Opzione-install Transparent Data Encryption (facoltativa) in SQL Server.</p></td>
<td align="left"><p>La funzionalità SQL Server di transcription esegue la crittografia di I/O in tempo reale e la decrittografia dei file di dati e di log, che possono aiutarti a rispettare numerose leggi, normative e linee guida stabilite in diversi settori.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Transparent esegue la decrittografia in tempo reale delle informazioni sul database, il che significa che, se l'account in cui è stato effettuato l'accesso ha le autorizzazioni per il database mentre si visualizzano le informazioni chiave di ripristino nelle tabelle di SQL Server, le informazioni sulla chiave di ripristino sono visibili.</p>
</div>
<div>

</div>
<p>Altre informazioni su Transparent: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 considerazioni sulla sicurezza</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>In SQL Server devono essere installati e eseguiti i servizi motore di database durante l'installazione di MBAM server.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Il servizio SQL Server Agent deve essere in funzione e impostato su avvio automatico nelle istanze selezionate di SQL Server.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Prerequisiti per il portale self-service

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
<td align="left"><p>Versione supportata di Windows Server</p>
<p>Vedi <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> MBAM 2,0 configurazioni supportate </a> per le versioni supportate.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 2,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)">Download di ASP.NET MVC 2</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Strumenti di gestione di IIS per servizi Web</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Prerequisiti per i client MBAM


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
<td align="left"><p><strong>I client Windows 7 </strong> - devono avere solo funzionalità Trusted Platform Module (TPM).</p></td>
<td align="left"><p>La versione TPM deve essere 1,2 o successiva.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Il chip TPM deve essere attivato nel BIOS e può essere ripristinato dal sistema operativo.</p></td>
<td align="left"><p>Per altre informazioni, vedere la documentazione del BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Solo client Windows 8 </strong> : per avere mbam Store e gestire le chiavi di ripristino del TPM: il provisioning automatico TPM deve essere disattivato e mbam deve essere impostato come proprietario del TPM prima di distribuire mbam. Per disattivare il provisioning automatico TPM, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</p>
<ul>
<li><p>Il provisioning automatico TPM deve essere disattivato.</p></li>
<li><p>MBAM deve essere impostato come proprietario del TPM prima di distribuire MBAM.</p></li>
</ul></td>
<td align="left"><p>Per disattivare il provisioning automatico TPM, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</p>
<div class="alert">
<strong>Nota</strong><br/><p>Verificare che la tastiera, il video o il mouse siano direttamente connessi e non gestiti tramite una tastiera, un video o un interruttore del mouse (KVM). Uno switch KVM può interferire con la capacità del computer di rilevare la presenza fisica dell'hardware.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Pianificazione della distribuzione di MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Configurazioni supportate di MBAM 2.0](mbam-20-supported-configurations-mbam-2.md)









