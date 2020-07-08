---
title: Considerazioni sulla sicurezza per MBAM 2.5
description: Considerazioni sulla sicurezza per MBAM 2.5
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826836"
---
# Considerazioni sulla sicurezza per MBAM 2.5


Questo argomento contiene le informazioni seguenti su come proteggere l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM):

-   [Configurare MBAM per escrow il TPM e archiviare le password di OwnerAuth](#bkmk-tpm)

-   [Configurare MBAM per sbloccare automaticamente il TPM dopo un blocco](#bkmk-autounlock)

-   [Connessioni sicure a SQL Server](#bkmk-secure-databases)

-   [Creare account e gruppi](#bkmk-accts-groups)

-   [Usare i file di log di MBAM](#bkmk-logfiles)

-   [Esaminare le considerazioni di database per i dati di MBAM](#bkmk-tde)

-   [Informazioni sulle considerazioni generali sulla sicurezza](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a>Configurare MBAM per escrow il TPM e archiviare le password di OwnerAuth

**Nota** Per Windows 10, versione 1607 o successiva, solo Windows può assumere la proprietà del TPM. Inoltre, Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM. Per ulteriori informazioni, vedere [password del proprietario del TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .

A seconda della configurazione in uso, il TPM (Trusted Platform Module) si bloccherà in determinate situazioni, ad esempio quando vengono immesse troppe password errate ─ e può rimanere bloccato per un periodo di tempo. Durante il blocco TPM, BitLocker non può accedere alle chiavi di crittografia per eseguire operazioni di sblocco o decrittografia, richiedendo all'utente di immettere la chiave di ripristino di BitLocker per accedere all'unità del sistema operativo. Per reimpostare il blocco TPM, è necessario specificare la password di OwnerAuth TPM.

MBAM può archiviare la password di OwnerAuth TPM nel database MBAM se è proprietaria del TPM o se ha escrowed la password. Le password di OwnerAuth sono quindi facilmente accessibili nel sito Web di amministrazione e monitoraggio quando è necessario eseguire il ripristino da un blocco TPM, eliminando la necessità di attendere che il blocco venga risolto autonomamente.

### Garanzia del TPM OwnerAuth in Windows 8 e versioni successive

**Nota** Per Windows 10, versione 1607 o successiva, solo Windows può assumere la proprietà del TPM. In addiiton Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM. Per ulteriori informazioni, vedere [password del proprietario del TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .

In Windows 8 o versioni successive, MBAM non deve più possedere il TPM per archiviare la password di OwnerAuth, purché il OwnerAuth sia disponibile nel computer locale.

Per abilitare MBAM a escrow e quindi archiviare le password di OwnerAuth TPM, è necessario configurare queste impostazioni di criteri di gruppo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Impostazione di criteri di gruppo</th>
<th align="left">Configurazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Attivare il backup TPM in servizi di dominio Active Directory</p></td>
<td align="left"><p>Disabilitata o non configurata</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare il livello delle informazioni di autorizzazione del proprietario del TPM disponibili per il sistema operativo</p></td>
<td align="left"><p>Delegata/nessuna o non configurata</p></td>
</tr>
</tbody>
</table>

 

La posizione di queste impostazioni di criteri di gruppo è la **configurazione dei computer** &gt; **modelli amministrativi** di &gt; **sistema** &gt; **Trusted Platform Module Services**.

**Nota**  Windows rimuove il OwnerAuth localmente dopo che MBAM l'ha esposta con successo con queste impostazioni.

 

### Garanzia del TPM OwnerAuth in Windows 7

In Windows 7, MBAM deve possedere il TPM per l'escrow automaticamente le informazioni di OwnerAuth del TPM nel database MBAM. Se MBAM non è il proprietario del TPM, è necessario usare i cmdlet di importazione di dati di MBAM Active Directory (AD) per copiare il TPM OwnerAuth da Active Directory nel database MBAM.

### MBAM cmdlet di importazione di dati di Active Directory

I cmdlet di importazione dei dati di MBAM Active Directory consentono di recuperare i pacchetti chiave di ripristino e le password di OwnerAuth archiviate in Active Directory.

Il server MBAM 2,5 SP1 viene fornito con quattro cmdlet di PowerShell che prepopolano i database di MBAM con le informazioni di ripristino del volume e del proprietario del TPM archiviate in Active Directory.

Per le chiavi e i pacchetti di ripristino del volume:

-   Read-ADRecoveryInformation

-   Write-MbamRecoveryInformation

Per informazioni sul proprietario del TPM:

-   Read-ADTpmInformation

-   Write-MbamTpmInformation

Per associare utenti ai computer:

-   Write-MbamComputerUser

I cmdlet Read-AD \ * leggono le informazioni da Active Directory. I cmdlet Write-mbam \ * spingono i dati nei database di MBAM. Per informazioni dettagliate su questi cmdlet, ad esempio sintassi, parametri ed esempi, vedere [riferimenti ai cmdlet per l'amministrazione e il monitoraggio di Microsoft Bitlocker 2,5](https://technet.microsoft.com/library/dn459018.aspx) .

**Creare associazioni da utente a computer:** I cmdlet di importazione dei dati di MBAM Active Directory raccolgono informazioni da Active Directory e inseriscono i dati in database MBAM. Tuttavia, non associano gli utenti ai volumi. È possibile scaricare lo script di PowerShell Add-ComputerUser.ps1 per creare associazioni da utente a computer, che consentono agli utenti di recuperare l'accesso a un computer tramite il sito Web di amministrazione e monitoraggio oppure usando il portale self-service per il ripristino. Lo script Add-ComputerUser.ps1 raccoglie i dati dall'attributo **Managed by** in Active Directory (ad), il proprietario dell'oggetto in un annuncio o da un file CSV personalizzato. Lo script aggiunge quindi gli utenti individuati all'oggetto della pipeline delle informazioni di ripristino, che deve essere passato a Write-MbamRecoveryInformation per inserire i dati nel database di ripristino.

Scaricare lo script di PowerShell Add-ComputerUser.ps1 dall' [area download Microsoft](https://go.microsoft.com/fwlink/?LinkId=613122).

Puoi specificare la **guida Add-ComputerUser.ps1** per ottenere assistenza per lo script, inclusi esempi su come usare i cmdlet e lo script.

Per creare associazioni da utente a computer dopo aver installato il server MBAM, usare il cmdlet di PowerShell Write-MbamComputerUser. In modo analogo allo script di PowerShell Add-ComputerUser.ps1, questo cmdlet consente di specificare gli utenti che possono usare il portale self-service per ottenere le informazioni OwnerAuth di TPM o le password di ripristino del volume per il computer specificato.

**Nota**  L'agente MBAM eseguirà l'override delle associazioni utente-computer quando il computer inizia a segnalare fino al server.

 

**Prerequisiti:** I cmdlet Read-AD \ * possono recuperare informazioni da Active Directory solo se vengono eseguiti come account utente con privilegi elevati, ad esempio un amministratore di dominio, o eseguiti come account in un gruppo di sicurezza personalizzato concesso l'accesso in lettura alle informazioni (scelta consigliata).

[Guida alle operazioni di crittografia unità BitLocker: il recupero dei volumi crittografati con servizi di dominio Active Directory](https://technet.microsoft.com/library/cc771778(WS.10).aspx) fornisce informazioni dettagliate sulla creazione di un gruppo di sicurezza personalizzato o di più gruppi con accesso in lettura alle informazioni sugli annunci.

**Autorizzazioni di scrittura per il recupero e il servizio Web hardware per mbam:** I cmdlet Write-mbam \ * accettano l'URL del servizio di ripristino e hardware di MBAM, usato per pubblicare le informazioni di ripristino o TPM. In genere, solo un account del servizio computer di dominio può comunicare con il servizio di ripristino e hardware di MBAM. In MBAM 2,5 SP1 è possibile configurare il servizio di ripristino e hardware di MBAM con un gruppo di sicurezza denominato DataMigrationAccessGroup i cui membri sono autorizzati a ignorare il controllo dell'account del servizio di computer del dominio. I cmdlet Write-mbam \ * devono essere eseguiti come utenti appartenenti a questo gruppo configurato. In alternativa, le credenziali di un singolo utente nel gruppo configurato possono essere specificate usando il parametro – Credential nei cmdlet Write-mbam \ *.

È possibile configurare il servizio di ripristino e hardware di MBAM con il nome del gruppo di sicurezza in uno dei modi seguenti:

-   Specificare il nome del gruppo di sicurezza (o individuale) nel parametro-DataMigrationAccessGroup del cmdlet Enable-MbamWebApplication-AgentService di PowerShell.

-   Configurare il gruppo dopo che il servizio di ripristino e hardware di MBAM è stato installato modificando il file di web.config nella &lt; &gt; cartella \\Microsoft di Solution\\Recovery e hardware Service\\ di Inetpub.

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    dove &lt; GroupName &gt; viene sostituito con il dominio e il nome del gruppo (o il singolo utente) che verrà usato per consentire la migrazione dei dati da Active Directory.

-   Usare l'editor di configurazione in Gestione IIS per modificare questo appSetting.

Nell'esempio seguente il comando, quando viene eseguito come membro del gruppo ADRecoveryInformation e del gruppo utenti migrazione dati, tirerà le informazioni di ripristino del volume dai computer nell'unità organizzativa WORKSTATION nel dominio contoso.com e li scriverà in MBAM usando il servizio di ripristino e hardware di MBAM in esecuzione nel server di mbam.contoso.com.

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

**Read-ad \ * cmdlet** accetta il nome o l'indirizzo IP di un computer server di hosting Active Directory in cui eseguire una query per le informazioni di ripristino o TPM. Ti consigliamo di fornire i nomi distinti dei contenitori di annunci in cui l'oggetto computer risiede come valore del parametro SearchBase. Se i computer sono archiviati in più unità organizzative, i cmdlet possono accettare l'input della pipeline da eseguire una sola volta per ogni contenitore. Il nome distinto di un contenitore di annunci avrà un aspetto simile a OU = machines, DC = contoso, DC = com. L'esecuzione di una ricerca mirata a specifici contenitori offre i vantaggi seguenti:

-   Riduce il rischio di timeout durante l'esecuzione di query su un set di dati di grandi dimensioni per gli oggetti computer.

-   Può omettere le UO che contengono Server Datacenter o altre classi di computer per cui il backup potrebbe non essere desiderato o necessario.

Un'altra opzione consiste nel specificare il flag-recurse con o senza il SearchBase facoltativo per cercare oggetti computer in tutti i contenitori in SearchBase specificato o nell'intero dominio rispettivamente. Quando usi il flag-recurse, puoi anche usare il parametro-MaxPageSize per controllare la quantità di memoria locale e remota necessaria per il servizio della query.

Questi cmdlet scrivono agli oggetti pipeline di tipo PsObject. Ogni istanza di PsObject contiene una sola chiave di ripristino del volume o una stringa del proprietario del TPM con il nome del computer associato, il timestamp e altre informazioni necessarie per pubblicarlo nell'archivio dati di MBAM.

**Write-mbam \ * i cmdlet** accettano i valori dei parametri delle informazioni di ripristino dalla pipeline per nome della proprietà. In questo modo, i cmdlet Write-mbam \ * accettano l'output della pipeline dei cmdlet Read-AD \ *, ad esempio Read-ADRecoveryInformation-server contoso.com-recurse | Write-MbamRecoveryInformation – RecoveryServiceEndpoint mbam.contoso.com).

I **cmdlet Write-mbam \ *** includono parametri facoltativi che offrono opzioni per la tolleranza di errore, la registrazione dettagliata e le preferenze per WhatIf e Confirm.

I **cmdlet Write-mbam \ *** includono anche un parametro di *ora* facoltativo il cui valore è un oggetto **DateTime** . Questo oggetto include un attributo *Kind* che può essere impostato su `Local` , `UTC` o `Unspecified` . Quando il parametro *Time* viene popolato da dati presi da Active Directory, l'ora viene convertita in UTC e questo attributo *Kind* viene impostato automaticamente su `UTC` . Tuttavia, quando si popola il parametro *Time* usando un'altra origine, ad esempio un file di testo, è necessario impostare esplicitamente l'attributo *Kind* sul relativo valore appropriato.

**Nota**  I cmdlet Read-AD \ * non hanno la possibilità di individuare gli account utente che rappresentano gli utenti del computer. Le associazioni di account utente sono necessarie per le operazioni seguenti:

-   Utenti per recuperare le password di volume/pacchetti usando il portale self-service

-   Utenti che non fanno parte del gruppo di sicurezza MBAM Advanced helpdesk Users come definito durante l'installazione, che si riprenderà per conto di altri utenti

 

## <a href="" id="bkmk-autounlock"></a>Configurare MBAM per sbloccare automaticamente il TPM dopo un blocco


È possibile configurare MBAM 2,5 SP1 per sbloccare automaticamente il TPM in caso di blocco. Se l'opzione di ripristino automatico del blocco TPM è abilitata, MBAM può rilevare che un utente è bloccato e quindi ottenere la password di OwnerAuth dal database MBAM per sbloccare automaticamente il TPM per l'utente. Blocco TPM il ripristino automatico è disponibile solo se la chiave di ripristino del sistema operativo per il computer è stata recuperata tramite il portale self service o il sito Web di amministrazione e monitoraggio.

**Importante**  Per abilitare la reimpostazione automatica del blocco TPM, è necessario configurare questa funzionalità sia nel lato server che in criteri di gruppo sul lato client.

 

-   Per abilitare la reimpostazione automatica del blocco TPM sul lato client, configurare l'impostazione di criteri di gruppo "Configura ripristino automatico di blocco TPM" disponibile in **Configurazione computer** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam** &gt; **Client Management**.

-   Per abilitare il ripristino automatico del blocco TPM sul lato server, è possibile selezionare "Abilita ripristino automatico del blocco TPM" nella configurazione guidata del server MBAM durante l'installazione.

    È anche possibile abilitare il ripristino automatico del blocco TPM in PowerShell specificando l'opzione "-TPM lockout auto reset" quando si Abilita il componente Web del servizio agente.

Dopo che un utente immette la chiave di ripristino di BitLocker ottenuta dal portale self service o dal sito Web di amministrazione e monitoraggio, l'agente di MBAM determinerà se il TPM è bloccato. Se è bloccata, tenterà di recuperare il OwnerAuth TPM per il computer dal database MBAM. Se il OwnerAuth TPM viene recuperato correttamente, verrà usato per sbloccare il TPM. Lo sblocco del TPM rende il TPM completamente funzionante e l'utente non verrà costretto a immettere la password di ripristino durante il riavvio successivo da un blocco TPM.

Il ripristino automatico del blocco TPM è disabilitato per impostazione predefinita.

**Nota**  Blocco TPM il ripristino automatico è supportato solo nei computer che eseguono il TPM versione 1,2. TPM 2,0 offre funzionalità di reimpostazione automatica del blocco predefinito.

 

**Il report di controllo del ripristino** include gli eventi correlati alla reimpostazione automatica del blocco TPM. Se viene effettuata una richiesta dal client MBAM per recuperare una password di OwnerAuth TPM, viene registrato un evento per indicare il ripristino. Le voci di controllo includono gli eventi seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voce</th>
<th align="left">Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Origine della richiesta di controllo</p></td>
<td align="left"><p>Sblocco TPM agente</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo di chiave</p></td>
<td align="left"><p>Hash della password TPM</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrizione motivo</p></td>
<td align="left"><p>Ripristino TPM</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a>Connessioni sicure a SQL Server


In MBAM, SQL Server comunica con SQL Server Reporting Services e con i servizi Web per il sito Web di amministrazione e monitoraggio e il portale self-service. È consigliabile proteggere la comunicazione con SQL Server. Per altre informazioni, vedere [crittografia di connessioni a SQL Server](https://technet.microsoft.com/library/ms189067.aspx).

Per altre informazioni su come proteggere i siti Web di MBAM, vedere [pianificazione di come proteggere i siti Web di mbam](planning-how-to-secure-the-mbam-websites.md).

## <a href="" id="bkmk-accts-groups"></a>Creare account e gruppi


La procedura consigliata per la gestione degli account utente consiste nel creare gruppi globali di dominio e aggiungere gli account utente. Per una descrizione degli account e dei gruppi consigliati, vedere [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).

## <a href="" id="bkmk-logfiles"></a>Usare i file di log di MBAM


Questa sezione descrive i file di log di MBAM server e MBAM client.

**File di log configurazione di MBAM server**

Il file **MBAMServerSetup.exe** genera i file di log seguenti nella cartella **% Temp%** dell'utente durante l'installazione di mbam:

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 Numbers &gt; . log**

    Registra le azioni intraprese durante l'installazione di MBAM e la configurazione della funzionalità del server MBAM.

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _numbers &gt;\_0\_MBAMServer.msi. log**

    Registra altre azioni intraprese durante l'installazione.

**File di log di configurazione di MBAM server**

-   **Registri delle applicazioni e dei servizi/Microsoft Windows/MBAM-Setup**

    Registra gli errori che si verificano quando si utilizzano i cmdlet di Windows PowerShell o la configurazione guidata server MBAM per configurare le caratteristiche del server MBAM.

**File di log della configurazione del client MBAM**

-   **MSI &lt; Five random characters &gt; . log**

    Registra le azioni intraprese durante l'installazione del client MBAM.

**MBAM-file di log Web**

-   Mostra le attività dei portali e dei servizi Web.

## <a href="" id="bkmk-tde"></a>Esaminare le considerazioni di database per i dati di MBAM


La funzionalità di crittografia dati trasparente (Transparent Data Encryption) disponibile in SQL Server è un'installazione facoltativa per le istanze di database che ospitano le caratteristiche del database MBAM.

Con Transparent, è possibile eseguire una crittografia a livello di database completa in tempo reale. Transparent è la scelta ottimale per la crittografia in blocco per soddisfare gli standard di sicurezza dei dati aziendali o conformità normativa. Transparent funziona a livello di file, che è simile a due caratteristiche di Windows: EFS (Encrypting File System) e crittografia unità BitLocker. Entrambe le funzionalità crittografano anche i dati nel disco rigido. Transparent non sostituisce crittografia a livello di cella, EFS o BitLocker.

Quando la funzionalità di crittografia è abilitata in un database, tutti i backup vengono crittografati. È quindi necessario prestare particolare attenzione per verificare che il certificato usato per proteggere la chiave di crittografia del database venga eseguito il backup e la manutenzione del database. Se il certificato (o i certificati) viene perduto, i dati saranno illeggibili.

Eseguire il backup del certificato con il database. Ogni backup del certificato deve avere due file. Entrambi i file devono essere archiviati. Idealmente per la sicurezza, è consigliabile eseguire il backup separatamente dal file di backup del database. In alternativa, puoi prendere in considerazione l'uso della funzionalità EKM (Extensible Key Management) (Vedi Extensible Key Management) per l'archiviazione e la manutenzione delle chiavi usate per Transparent.

Per un esempio di come abilitare Transparent per le istanze di database di MBAM, vedere [informazioni sulla crittografia dei dati trasparente](https://technet.microsoft.com/library/bb934049.aspx)

## <a href="" id="bkmk-general-security"></a>Informazioni sulle considerazioni generali sulla sicurezza


**Comprendere i rischi per la sicurezza.** Il rischio più grave quando si usa l'amministrazione e il monitoraggio di Microsoft BitLocker è che la sua funzionalità potrebbe essere compromessa da un utente non autorizzato che potrebbe quindi riconfigurare la crittografia unità BitLocker e ottenere i dati della chiave di crittografia BitLocker nei client MBAM. Tuttavia, la perdita delle funzionalità di MBAM per un breve periodo di tempo, a causa di un attacco di tipo Denial of Service, in genere non ha un impatto catastrofico, a differenza, ad esempio, di perdere posta elettronica o comunicazioni di rete o di alimentazione.

**Proteggere fisicamente i computer**. Non c'è sicurezza senza sicurezza fisica. Un utente malintenzionato che ottiene l'accesso fisico a un server MBAM può potenzialmente usarlo per attaccare l'intera base client. Tutti i potenziali attacchi fisici devono essere considerati ad alto rischio e mitigati in modo appropriato. I server MBAM devono essere archiviati in una sala server sicura con accesso controllato. Proteggere questi computer quando gli amministratori non sono fisicamente presenti quando il sistema operativo blocca il computer oppure usando uno screen saver protetto.

**Applicare gli aggiornamenti della sicurezza più recenti a tutti i computer**. Rimanere informati sui nuovi aggiornamenti per sistemi operativi Windows, SQL Server e MBAM iscrivendoti al servizio di notifica della sicurezza presso il [TechCenter di sicurezza](https://go.microsoft.com/fwlink/?LinkId=28819).

**Usare password complesse o passare frasi**. Usa sempre password complesse con 15 o più caratteri per tutti gli account di amministratore di MBAM. Non usare mai password vuote. Per altre informazioni sui concetti relativi alle password, vedere [criteri password](https://technet.microsoft.com/library/hh994572.aspx).



## Argomenti correlati


[Pianificazione della distribuzione di MBAM 2.5](planning-to-deploy-mbam-25.md)

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





