---
title: Controllare le chiavi del Registro di sistema prima di installare il server App-V 5.x
description: Controllare le chiavi del Registro di sistema prima di installare il server App-V 5.x
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805931"
---
# Controllare le chiavi del Registro di sistema prima di installare il server App-V 5.x

Se si sta aggiornando il pacchetto di hotfix App-v 5,0 SP1 3 o versione successiva, eseguire i passaggi descritti in questa sezione prima di installare il server App-V 5. x

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Quando è necessario eseguire questo passaggio</strong></p></td>
<td align="left"><p>Si esegue l'aggiornamento da App-V 5,0 SP1 con i successivi pacchetti di hotfix installati usando un file msp.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Quali componenti richiedono di eseguire questo passaggio</strong></p></td>
<td align="left"><p>Solo i componenti di App-V Server che si stanno aggiornando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Quando è necessario eseguire questo passaggio</strong></p></td>
<td align="left"><p>Prima di aggiornare l'App-V Server in App-V 5. x</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Cosa è necessario fare</strong></p></td>
<td align="left"><p>Usando le informazioni nelle tabelle seguenti, aggiornare ogni valore della chiave del registro <code>HKLM\Software\Microsoft\AppV\Server</code> di sistema in con il valore specificato nell'installazione del server originale. Il completamento di questo passaggio ripristina i valori del registro di sistema che potrebbero essere stati rimossi quando sono stati installati i pacchetti di hotfix di App-V 5,0 SP1.</p></td>
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

