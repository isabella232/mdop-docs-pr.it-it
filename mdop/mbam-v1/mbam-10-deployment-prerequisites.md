---
title: Prerequisiti per la distribuzione di MBAM 1.0
description: Prerequisiti per la distribuzione di MBAM 1.0
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822665"
---
# Prerequisiti per la distribuzione di MBAM 1.0


Prima di iniziare l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM), verificare di soddisfare i prerequisiti necessari per installare il prodotto. Questa sezione contiene informazioni utili per preparare correttamente l'ambiente di elaborazione prima di distribuire i client e le funzionalità del server di MBAM.

## Prerequisiti di installazione per le caratteristiche del server MBAM


Ogni funzionalità di MBAM Server include prerequisiti specifici che devono essere soddisfatti prima che possano essere installati correttamente. MBAM setup verifica se tutti i prerequisiti vengono soddisfatti prima che l'installazione venga avviata.

### Prerequisiti di installazione per l'amministrazione e il server di monitoraggio

La tabella seguente contiene i prerequisiti di installazione per l'amministrazione e il server di monitoraggio di MBAM:

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
<td align="left"><p><strong>Ruolo del server di Windows ServerWeb</strong></p></td>
<td align="left"><p>Questo ruolo deve essere aggiunto a un sistema operativo server supportato per la funzionalità mbam Administration e Monitoring Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Strumenti di gestione di Web Server (IIS)</strong></p></td>
<td align="left"><p><strong>Script e strumenti di gestione di IIS</strong></p></td>
</tr>
<tr class="odd">
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
<tr class="even">
<td align="left"><p><strong>Caratteristiche di Windows Server</strong></p></td>
<td align="left"><p><strong>Caratteristiche di Microsoft .NET Framework 3.5.1:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>Attivazione di WCF</p>
<ul>
<li><p>Attivazione HTTP</p></li>
<li><p>Attivazione non HTTP</p></li>
</ul></li>
</ul>
<p><strong>Servizio Attivazione dei processi Windows</strong></p>
<ul>
<li><p>Modello di processo</p></li>
<li><p>Ambiente .NET</p></li>
<li><p>API di configurazione</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Nota**  Per un elenco dei sistemi operativi supportati, Vedi le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).

 

### Prerequisiti di installazione per i report di conformità e controllo

I report di conformità e controllo devono essere installati in una versione supportata di SQLServer. I prerequisiti di installazione per questa funzionalità includono SQL Server Reporting Services (SSRS).

SSRS deve essere installato ed eseguito durante l'installazione di MBAM server. La funzione SSRS deve essere configurata anche in modalità "nativa", non nella modalità "non configurata" o "SharePoint".

**Nota**  Per un elenco dei sistemi operativi supportati e delle versioni di SQLServer, Vedi le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).

 

### Prerequisiti di installazione per il database di ripristino e hardware

Il database di ripristino e hardware deve essere installato in una versione supportata di SQLServer.

SQL Server deve avere installato ed eseguito i servizi motore di database durante l'installazione di MBAM server. È necessario abilitare la caratteristica Transparent Data Encryption.

**Nota**  Per un elenco dei sistemi operativi supportati e delle versioni di SQLServer, Vedi le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).

 

La caratteristica di Transcript SQLServer consente di eseguire la crittografia di input/output (I/O) in tempo reale dei file di dati e di log. Transparent protegge i dati "a riposo", che includono i dati e i file di log. Offre la possibilità di rispettare numerose leggi, normative e linee guida stabilite in diversi settori.

**Nota**  Dato che la crittografia in tempo reale viene eseguita per la decrittazione delle informazioni sul database, le informazioni sulla chiave di ripristino saranno visibili se l'account in cui è stato effettuato l'accesso dispone delle autorizzazioni per il database quando si visualizzano le tabelle SQL delle informazioni chiave di ripristino.

 

### Prerequisiti di installazione per il database di conformità e controllo

Il database di conformità e controllo deve essere installato in una versione supportata di SQLServer.

In SQL Server devono essere installati e eseguiti i servizi motore di database durante l'installazione di MBAM server.

**Nota**  Per un elenco dei sistemi operativi supportati e delle versioni di SQLServer, Vedi le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).

 

## Prerequisiti di installazione per i client MBAM


I prerequisiti necessari che è necessario soddisfare prima di iniziare l'installazione del client MBAM sono i seguenti:

-   Funzionalità TPM (Trusted Platform Module) v 1.2

-   Il chip TPM deve essere attivato nel BIOS e deve essere ripristinato dal sistema operativo. Per altre informazioni, vedere la documentazione del BIOS.

**Avviso**  Verificare che la tastiera, il mouse e il video siano collegati direttamente al computer, anziché a un interruttore di tastiera, video, mouse (KVM). Uno switch KVM può interferire con la capacità del computer di rilevare la presenza fisica dell'hardware.

 

## Argomenti correlati


[Pianificazione della distribuzione di MBAM 1.0](planning-to-deploy-mbam-10.md)

[Configurazioni supportate di MBAM 1.0](mbam-10-supported-configurations.md)

 

 





