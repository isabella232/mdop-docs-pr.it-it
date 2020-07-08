---
title: Come usare una riga di comando per installare il server MBAM
description: Come usare una riga di comando per installare il server MBAM
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825645"
---
# Come usare una riga di comando per installare il server MBAM


È possibile usare una riga di comando per installare il server MBAM con la topologia autonoma o Gestione configurazione. L'esempio della riga di comando seguente è per la distribuzione di MBAM in un singolo server, che è un'architettura che deve essere usata solo in un ambiente di test. Sarà necessario cambiare la riga di comando di conseguenza quando si distribuisce MBAM in un ambiente di produzione, che dovrebbe avere più server.

## Riga di comando per la distribuzione del server MBAM 2.0 con la topologia autonoma


È possibile usare una riga di comando simile alla seguente per installare il server MBAM con la topologia autonoma.

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

La tabella seguente descrive i parametri della riga di comando per la distribuzione del server MBAM con la topologia autonoma.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parametro</th>
<th align="left">Valore di parametro</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TOPOLOGIA</p></td>
<td align="left"><p>0</p></td>
<td align="left"><p>0-topologia autonoma</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>01</p></td>
<td align="left"><p>0-non accettare la licenza agreement1-accettare il contratto di licenza</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADDLOCAL</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Caratteristiche da installare nel server</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Database</p></td>
<td align="left"><p>Database di ripristino</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>ReportsDatabase</p></td>
<td align="left"><p>Database dei report di conformità e controllo</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Rapporti</p></td>
<td align="left"><p>Report di conformità e controllo</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>AdministrationMonitoringServer</p></td>
<td align="left"><p>Sito Web di amministrazione e monitoraggio</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>SelfServiceServer</p></td>
<td align="left"><p>Portale self-service</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>PolicyTemplate</p></td>
<td align="left"><p>Modello di criteri di gruppo di MBAM</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>UserDomain [UserName1]</p></td>
<td align="left"><p>Dominio e account utente dell'account del servizio Reporting Services che accede al database di conformità e controllo</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Password dell'account del servizio Reporting Services che accederà al database di conformità e controllo</p></td>
</tr>
<tr class="even">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Nome istanza di SQL Server per il database di conformità e controllo: Sostituisci <strong> % nomecomputer% </strong> con il nome del computer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Nome istanza di SQL Server per il database di ripristino: Sostituisci <strong> % nomecomputer% </strong> con il nome del computer</p></td>
</tr>
<tr class="even">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Istanza di SQL Server Reporting Server in cui verranno installati i report di conformità e controllo-Sostituisci <strong> % nomecomputer% </strong> con il nome del computer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Porta per il sito Web di amministrazione e monitoraggio; "83" è solo un esempio</p></td>
</tr>
<tr class="even">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Porta per il sito Web portale self-service; "83" è solo un esempio</p></td>
</tr>
</tbody>
</table>

 

## Riga di comando per la distribuzione del server MBAM 2.0 con la topologia di Configuration Manager


Per installare il server MBAM con la topologia di Configuration Manager, è possibile usare una riga di comando simile alla seguente.

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

La tabella seguente descrive i parametri della riga di comando per l'installazione del server MBAM 2.0 con la topologia di Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parametro</th>
<th align="left">Valore di parametro</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TOPOLOGIA</p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>1-topologia di Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>01</p></td>
<td align="left"><p>0-non accettare la licenza agreement1-accettare il contratto di licenza</p></td>
</tr>
<tr class="odd">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Nome istanza di SQL Server per il database di controllo: Sostituisci <strong> % nomecomputer% </strong> con il nome del computer</p></td>
</tr>
<tr class="even">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Nome istanza di SQL Server per il database di ripristino-sostituire <strong> % nomecomputer% </strong> con il nome del computer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Istanza di SQL Server Reporting Server in cui verranno installati i report di controllo, sostituire% NomeComputer% con il nome del computer</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>UserDomain [UserName1]</p></td>
<td align="left"><p>Dominio e account utente dell'account del servizio Reporting Services che accede al database di conformità e controllo</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Password dell'account del servizio Reporting Services che accederà al database di conformità e controllo</p></td>
</tr>
<tr class="even">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Porta per il sito Web di amministrazione e monitoraggio; "83" è solo un esempio</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Porta per il sito Web portale self-service; "83" è solo un esempio</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Distribuzione dell'infrastruttura server di MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





