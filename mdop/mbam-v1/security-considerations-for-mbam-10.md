---
title: Considerazioni sulla sicurezza per MBAM 1.0
description: Considerazioni sulla sicurezza per MBAM 1.0
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826195"
---
# Considerazioni sulla sicurezza per MBAM 1.0


Questo argomento contiene una breve panoramica degli account e dei gruppi, i file di log e altre considerazioni relative alla sicurezza per Microsoft BitLocker Administration and Monitoring (MBAM). Per altre informazioni, seguire i collegamenti in questo articolo.

## Considerazioni generali sulla sicurezza


**Comprendere i rischi per la sicurezza.** Il rischio più grave per MBAM è che la sua funzionalità potrebbe essere dirottata da un utente non autorizzato che potrebbe quindi riconfigurare la crittografia BitLocker e ottenere i dati della chiave di crittografia BitLocker nei client MBAM. Tuttavia, la perdita delle funzionalità di MBAM per un breve periodo di tempo a causa di un attacco di tipo Denial of Service non avrebbe in genere un impatto catastrofico.

**Proteggere fisicamente i computer**. La sicurezza è incompleta senza sicurezza fisica. Chiunque abbia accesso fisico a un server MBAM potrebbe potenzialmente attaccare l'intera base client. Eventuali attacchi fisici potenziali devono essere considerati ad alto rischio e mitigati in modo appropriato. I server MBAM devono essere archiviati in una sala server fisicamente sicura con accesso controllato. Proteggere questi computer quando gli amministratori non sono fisicamente presenti quando il sistema operativo blocca il computer oppure usando uno screen saver protetto.

**Applicare gli aggiornamenti della sicurezza più recenti a tutti i computer**. Tieniti aggiornato sui nuovi aggiornamenti per i sistemi operativi, Microsoft SQL Server e MBAM iscrivendoti al servizio di notifica della sicurezza <https://go.microsoft.com/fwlink/p/?LinkId=28819> .

**Usare password complesse o passare frasi**. Usa sempre password complesse con 15 o più caratteri per tutti gli account di amministratore di MBAM e MBAM. Non usare mai password vuote. Per altre informazioni sui concetti relativi alle password, vedere il white paper "account password e criteri" su TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).

## Account e gruppi in MBAM


Una procedura consigliata per la gestione degli account utente consiste nel creare gruppi globali di dominio e aggiungere gli account utente. Quindi, Aggiungi gli account globali di dominio ai gruppi di MBAM locali necessari nei server MBAM.

### Gruppi di ActiveDirectoryDomainServices

Nessun gruppo viene creato automaticamente durante la configurazione di MBAM. Devi tuttavia creare i seguenti gruppi globali di ActiveDirectoryDomainServices per gestire le operazioni di MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome del gruppo</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM Advanced helpdesk utenti</p></td>
<td align="left"><p>Crea questo gruppo per gestire i membri del gruppo locale degli utenti di MBAM Advanced helpdesk che è stato creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controllo di conformità MBAM per l'accesso DB</p></td>
<td align="left"><p>Creare questo gruppo per gestire i membri del gruppo di controllo della conformità MBAM di DB Access che è stato creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utenti di hardware MBAM</p></td>
<td align="left"><p>Creare questo gruppo per gestire i membri del gruppo di utenti hardware MBAM che è stato creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utenti di MBAM helpdesk</p></td>
<td align="left"><p>Creare questo gruppo per gestire i membri del gruppo di utenti di MBAM helpdesk locale creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Accesso di MBAM e DB hardware</p></td>
<td align="left"><p>Crea questo gruppo per gestire i membri del gruppo locale per il recupero e il ripristino di MBAM e l'hardware che è stato creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utenti di report MBAM</p></td>
<td align="left"><p>Creare questo gruppo per gestire i membri del gruppo di utenti del report MBAM che è stato creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Amministratori di sistema MBAM</p></td>
<td align="left"><p>Crea questo gruppo per gestire i membri del gruppo di amministratori di sistema MBAM che è stato creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Esenzioni crittografiche di BitLocker</p></td>
<td align="left"><p>Creare questo gruppo per gestire gli account utente che devono essere esentati dalla crittografia BitLocker a partire da computer a cui accedono.</p></td>
</tr>
</tbody>
</table>

 

### Gruppi locali di MBAM server

MBAM setup crea gruppi locali per supportare le operazioni di MBAM. Dovresti aggiungere i gruppi globali di ActiveDirectoryDomainServices ai gruppi locali di MBAM appropriati per configurare le autorizzazioni di sicurezza e accesso ai dati di MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome del gruppo</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM Advanced helpdesk utenti</p></td>
<td align="left"><p>I membri di questo gruppo hanno esteso l'accesso alle funzionalità dell'helpdesk di amministrazione e monitoraggio di Microsoft BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controllo di conformità MBAM per l'accesso DB</p></td>
<td align="left"><p>Questo gruppo contiene i computer che hanno accesso al database di controllo di conformità di MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utenti di hardware MBAM</p></td>
<td align="left"><p>I membri di questo gruppo hanno accesso ad alcune delle funzionalità di funzionalità hardware dell'amministrazione e del monitoraggio di Microsoft BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utenti di MBAM helpdesk</p></td>
<td align="left"><p>I membri di questo gruppo hanno accesso ad alcune delle funzionalità dell'helpdesk dall'amministrazione e dal monitoraggio di Microsoft BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Accesso di MBAM e DB hardware</p></td>
<td align="left"><p>Questo gruppo contiene i computer che hanno accesso al database di MBAM Recovery e hardware.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utenti di report MBAM</p></td>
<td align="left"><p>I membri di questo gruppo hanno accesso ai report di conformità e controllo dall'amministrazione e dal monitoraggio di Microsoft BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Amministratori di sistema MBAM</p></td>
<td align="left"><p>I membri di questo gruppo hanno accesso a tutte le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker.</p></td>
</tr>
</tbody>
</table>

 

### Account di accesso di report SSRS

L'account del servizio report di SQL Server Reporting Services (SSRS) fornisce il contesto di sicurezza per l'esecuzione dei report di MBAM disponibili tramite SSRS. Questo account è configurato durante la configurazione di MBAM.

## File di log di MBAM


Durante la configurazione di MBAM, i seguenti file di log di configurazione di MBAM vengono creati nella cartella% Temp% dell'utente che installa il

**File di log configurazione di MBAM server**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; Five random characters &gt; </em> . log  
Registra le azioni intraprese durante l'installazione di MBAM Setup e MBAM server.

<a href="" id="installcompliancedatabase-log"></a>InstallComplianceDatabase. log  
Registra le azioni intraprese per creare la configurazione del database di stato di conformità di MBAM.

<a href="" id="installkeycompliancedatabase-log"></a>InstallKeyComplianceDatabase. log  
Registra le azioni intraprese per creare il database di ripristino e hardware di MBAM.

<a href="" id="addhelpdeskdbauditusers-log"></a>AddHelpDeskDbAuditUsers. log  
Registra le azioni intraprese per creare gli account di accesso di SQL Server nel database di stato della conformità di MBAM e autorizzare il servizio Web Helpdesk nel database per i report.

<a href="" id="addhelpdeskdbusers-log"></a>AddHelpDeskDbUsers. log  
Registra le azioni intraprese per autorizzare i servizi Web al database per il ripristino delle chiavi e creare gli account di accesso al database hardware e ripristino di MBAM.

<a href="" id="addkeycompliancedbusers-log"></a>AddKeyComplianceDbUsers. log  
Registra le azioni intraprese per autorizzare i servizi Web al database di stato di conformità MBAM per la creazione di report di conformità.

<a href="" id="addrecoveryandhardwaredbusers-log"></a>AddRecoveryAndHardwareDbUsers. log  
Registra le azioni intraprese per autorizzare servizi Web per il ripristino di MBAM e il database hardware per il ripristino della chiave.

**Nota**  Per ottenere altri file di log della configurazione di MBAM, è necessario installare l'amministrazione e il monitoraggio di Microsoft BitLocker tramite il pacchetto **msiexec** e l'opzione di posizione **/l** &lt; &gt; . I file di log vengono creati nella posizione specificata.

 

**File di log della configurazione del client MBAM**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; Five random characters &gt; </em> . log  
Registra le azioni intraprese durante l'installazione del client MBAM.

## Considerazioni su dati di database di MBAM


La funzionalità di crittografia dati trasparente (Transparent Data Encryption) disponibile in SQL Server 2008 è un requisito necessario per l'installazione delle istanze di database che ospiteranno le caratteristiche del database MBAM.

Con Transparent, è possibile eseguire una crittografia a livello di database completa in tempo reale. Transparent è una scelta adatta per la crittografia in blocco per soddisfare gli standard di sicurezza dei dati aziendali o conformità normativa. Transparent funziona a livello di file, che è simile a due caratteristiche di Windows: EFS (Encrypting File System) e crittografia unità BitLocker, entrambi i quali crittografano anche i dati nel disco rigido. Transparent non sostituisce crittografia a livello di cella, EFS o BitLocker.

Quando la funzionalità di crittografia è abilitata in un database, tutti i backup vengono crittografati. È quindi necessario prestare particolare attenzione per garantire che il certificato usato per proteggere la chiave di crittografia del database (decifratore) sia supportato e mantenuto con il backup del database. Senza un certificato, i dati saranno illeggibili. Eseguire il backup del certificato insieme al database. Ogni backup del certificato deve avere due file; entrambi i file devono essere archiviati. È consigliabile archiviarli separatamente dal file di backup del database per la sicurezza.

Per un esempio di come abilitare le istanze di Transparent per il database MBAM, vedere [valutazione di mbam 1,0](evaluating-mbam-10.md).

Per altre informazioni su Transparent in SQLServer 2008, vedere [crittografia di database in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).

## Argomenti correlati


[Sicurezza e privacy per MBAM 1.0](security-and-privacy-for-mbam-10.md)

 

 





