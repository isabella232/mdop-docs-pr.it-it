---
title: Considerazioni sulla sicurezza per MBAM 2.0
description: Considerazioni sulla sicurezza per MBAM 2.0
author: dansimp
ms.assetid: 0aa5c6e2-d92c-4e30-9f6a-b48abb667ae5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 04dc9b667faddecab629b50f4c5d909fd7b2829e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823915"
---
# Considerazioni sulla sicurezza per MBAM 2.0


Questo argomento contiene una breve panoramica sugli account e i gruppi, i file di log e altre considerazioni relative alla sicurezza per Microsoft BitLocker Administration and Monitoring (MBAM). Per altre informazioni, seguire i collegamenti contenuti in questo articolo.

## Considerazioni generali sulla sicurezza


**Comprendere i rischi per la sicurezza.** Il rischio più grave per l'amministrazione e il monitoraggio di Microsoft BitLocker è che la sua funzionalità potrebbe essere dirottata da un utente non autorizzato che potrebbe quindi riconfigurare la crittografia BitLocker e ottenere i dati della chiave di crittografia BitLocker nei client MBAM. Tuttavia, la perdita di funzionalità di MBAM per un breve periodo di tempo, a causa di un attacco di tipo Denial of Service, in genere non ha un impatto catastrofico, a differenza, ad esempio, posta elettronica, comunicazioni di rete, luce e alimentazione.

**Proteggere fisicamente i computer**. Non c'è sicurezza senza sicurezza fisica. Un utente malintenzionato che ottiene l'accesso fisico a un server MBAM può potenzialmente usarlo per attaccare l'intera base client. Tutti i potenziali attacchi fisici devono essere considerati ad alto rischio e mitigati in modo appropriato. I server MBAM devono essere archiviati in una sala server sicura con accesso controllato. Proteggere questi computer quando gli amministratori non sono fisicamente presenti quando il sistema operativo blocca il computer oppure usando uno screen saver protetto.

**Applicare gli aggiornamenti della sicurezza più recenti a tutti i computer**. Tieniti aggiornato sui nuovi aggiornamenti per i sistemi operativi, Microsoft SQL Server e MBAM iscrivendoti al servizio di notifica della sicurezza <https://go.microsoft.com/fwlink/?LinkId=28819> .

**Usare password complesse o passare frasi**. Usa sempre password complesse con 15 o più caratteri per tutti gli account di amministratore di MBAM e MBAM. Non usare mai password vuote. Per altre informazioni sui concetti relativi alle password, vedere il white paper "account password e criteri" su TechNet ( <https://go.microsoft.com/fwlink/?LinkId=30009> ).

## Account e gruppi in MBAM


La procedura consigliata per la gestione degli account utente consiste nel creare gruppi globali di dominio e aggiungere gli account utente. Quindi, Aggiungi gli account globali di dominio ai gruppi di MBAM locali necessari nei server MBAM.

### Gruppi di ActiveDirectoryDomainServices

Nessun gruppo di Active Directory viene creato automaticamente durante il processo di configurazione di MBAM. Tuttavia, è consigliabile creare i gruppi globali di ActiveDirectoryDomainServices seguenti per gestire le operazioni di MBAM.

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
<td align="left"><p>Creare questo gruppo per gestire i membri del gruppo locale degli utenti di MBAM Advanced helpdesk creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controllo di conformità MBAM per l'accesso DB</p></td>
<td align="left"><p>Creare questo gruppo per gestire i membri del gruppo di controllo della conformità di MBAM DB Access locale creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utenti di MBAM helpdesk</p></td>
<td align="left"><p>Creare questo gruppo per gestire i membri del gruppo di utenti di MBAM helpdesk locale creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Accesso di MBAM e DB hardware</p></td>
<td align="left"><p>Crea questo gruppo per gestire i membri del gruppo locale per il recupero e il ripristino di MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utenti di report MBAM</p></td>
<td align="left"><p>Creare questo gruppo per gestire i membri del gruppo di utenti del report MBAM creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Amministratori di sistema MBAM</p></td>
<td align="left"><p>Creare questo gruppo per gestire i membri del gruppo di amministratori di sistema MBAM creato durante la configurazione di MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Esenzioni crittografiche di BitLocker</p></td>
<td align="left"><p>Creare questo gruppo per gestire gli account utente che devono essere esentati dalla crittografia BitLocker a partire da computer a cui accedono.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> Gruppi locali di MBAM server

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
<td align="left"><p>I membri di questo gruppo hanno aumentato l'accesso alle funzionalità dell'help desk di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controllo di conformità MBAM per l'accesso DB</p></td>
<td align="left"><p>Contiene i computer che hanno accesso al database di controllo e conformità di MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utenti di MBAM helpdesk</p></td>
<td align="left"><p>I membri di questo gruppo hanno accesso ad alcune delle funzionalità dell'help desk di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Accesso di MBAM e DB hardware</p></td>
<td align="left"><p>Contiene i computer che hanno accesso al database di ripristino di MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utenti di report MBAM</p></td>
<td align="left"><p>I membri di questo gruppo hanno accesso ai report di conformità e controllo di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Amministratori di sistema MBAM</p></td>
<td align="left"><p>I membri di questo gruppo hanno accesso a tutte le caratteristiche di MBAM.</p></td>
</tr>
</tbody>
</table>

 

### Account del servizio report SSRS

L'account del servizio report SSRS fornisce il contesto di sicurezza per l'esecuzione dei report di MBAM disponibili tramite SSRS. È configurato durante la configurazione di MBAM.

Quando si configura l'account del servizio report SSRS, specificare un account utente di dominio e configurare la password per non scadere mai.

**Nota**  Se si modifica il nome dell'account del servizio dopo la distribuzione di MBAM, è necessario riconfigurare l'origine dati dei report per usare le nuove credenziali dell'account del servizio. In caso contrario, non sarà possibile accedere al portale help desk.

 

## <a href="" id="---------mbam-log-files"></a> File di log di MBAM


I file di log di configurazione di MBAM seguenti vengono creati nella cartella% Temp% dell'utente di installazione durante l'installazione di MBAM:

**File di log configurazione di MBAM server**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; Five random characters &gt; </em> . log  
Registra le azioni intraprese durante l'installazione di MBAM Setup e MBAM server.

<a href="" id="installcompliancedatabase-log"></a>InstallComplianceDatabase. log  
Registra le azioni intraprese per creare la conformità MBAM e la configurazione del database di audit.

<a href="" id="installkeycompliancedatabase-log"></a>InstallKeyComplianceDatabase. log  
Registra le azioni intraprese per creare il database di ripristino MBAM.

<a href="" id="addhelpdeskdbauditusers-log"></a>AddHelpDeskDbAuditUsers. log  
Registra le azioni intraprese per creare gli account di accesso di SQL Server nel database di controllo e conformità di MBAM e autorizzare il servizio Web HelpDesk nel database per i report.

<a href="" id="addhelpdeskdbusers-log"></a>AddHelpDeskDbUsers. log  
Registra le azioni intraprese per autorizzare i servizi Web al database per il ripristino delle chiavi e creare account di accesso al database di ripristino MBAM.

<a href="" id="addkeycompliancedbusers-log"></a>AddKeyComplianceDbUsers. log  
Registra le azioni intraprese per autorizzare i servizi Web a eseguire MBAM compliance e database di audit per i report di conformità.

<a href="" id="addrecoveryandhardwaredbusers-log"></a>AddRecoveryAndHardwareDbUsers. log  
Registra le azioni adottate per autorizzare i servizi Web al database di ripristino di MBAM per il ripristino della chiave.

**Nota**  Per ottenere ulteriori file di log di MBAM Setup, è necessario installare MBAM usando il pacchetto msiexec e l' &lt; opzione di posizione/l &gt; . I file di log vengono creati nella posizione specificata.

 

**File di log della configurazione del client MBAM**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; Five random characters &gt; </em> . log  
Registra le azioni intraprese durante l'installazione del client MBAM.

## <a href="" id="---------mbam-database-tde-considerations"></a> Considerazioni su dati di database di MBAM


La funzionalità di crittografia dati trasparente (Transparent Data Encryption) disponibile in SQL Server è un'installazione facoltativa per le istanze di database che ospitano le caratteristiche del database MBAM.

Con Transparent, è possibile eseguire una crittografia a livello di database completa in tempo reale. Transparent è la scelta ottimale per la crittografia in blocco per soddisfare gli standard di sicurezza dei dati aziendali o conformità normativa. Transparent funziona a livello di file, che è simile a due caratteristiche di Windows: EFS (Encrypting File System) e crittografia unità BitLocker, entrambi i quali crittografano anche i dati nel disco rigido. Transparent non sostituisce crittografia a livello di cella, EFS o BitLocker.

Quando la funzionalità di crittografia è abilitata in un database, tutti i backup vengono crittografati. È quindi necessario prestare particolare attenzione per verificare che il certificato usato per proteggere la chiave di crittografia del database venga eseguito il backup e la manutenzione del database. Se il certificato (o i certificati) viene perduto, i dati saranno illeggibili. Eseguire il backup del certificato insieme al database. Ogni backup del certificato deve avere due file. Entrambi i file devono essere archiviati (in modo ideale separatamente dal file di backup del database per la sicurezza). In alternativa, puoi prendere in considerazione l'uso della funzionalità EKM (Extensible Key Management) (Vedi Extensible Key Management) per l'archiviazione e la manutenzione delle chiavi usate per Transparent.

Per un esempio di come abilitare le istanze di Transparent per il database MBAM, vedere [valutazione di mbam 2,0](evaluating-mbam-20-mbam-2.md).

Per altre informazioni su Transparent in SQLServer 2008, vedere [crittografia di SQL Server]( https://go.microsoft.com/fwlink/?LinkId=299883).

## Argomenti correlati


[Sicurezza e privacy per MBAM 2.0](security-and-privacy-for-mbam-20-mbam-2.md)

 

 





