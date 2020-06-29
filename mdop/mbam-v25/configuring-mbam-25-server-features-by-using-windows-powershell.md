---
title: Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell
description: Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822836"
---
# Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell


Dopo aver installato il software del server MBAM 2,5, è possibile usare le funzionalità configura MBAM 2,5 server usando i cmdlet di Windows PowerShell o la configurazione guidata server di MBAM. Questo argomento descrive come configurare MBAM 2,5 usando i cmdlet di Windows PowerShell. Per usare la procedura guidata, vedere [configurazione delle funzionalità del server MBAM 2,5](configuring-the-mbam-25-server-features.md).

## Contenuto dell'argomento


Questo argomento include le informazioni seguenti sull'uso di Windows PowerShell per configurare MBAM:

-   [Come caricare la Guida di Windows PowerShell per MBAM 2,5](#bkmk-load-posh-help)

-   [Come ottenere assistenza per un cmdlet di Windows PowerShell di MBAM](#bkmk-help-specific-cmdlet)

-   [Configurazioni che è possibile eseguire solo con Windows PowerShell, ma non con la configurazione guidata del server MBAM](#bkmk-config-only-posh)

-   [Prerequisiti e requisiti per l'uso di Windows PowerShell per configurare le caratteristiche del server MBAM](#bkmk-prereqs-posh-mbamsvr)

-   [Uso di Windows PowerShell per configurare MBAM in un computer remoto](#bkmk-remote-config)

-   [Account obbligatori e parametri del cmdlet di Windows PowerShell corrispondenti](#bkmk-reqd-posh-accts)

Per informazioni sui cmdlet **Get-MbamBitLockerRecoveryKey** e **Get-MbamTPMOwnerPassword** di Windows PowerShell, che vengono usati per amministrare mbam, vedere [uso di Windows powershell per amministrare MBAM 2,5](using-windows-powershell-to-administer-mbam-25.md).

## <a href="" id="bkmk-load-posh-help"></a>Come caricare la Guida di Windows PowerShell per MBAM 2,5


Per un elenco dei cmdlet di Windows PowerShell in TechNet, vedere [automazione di Microsoft Desktop Optimization Pack con Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).

**Per caricare la Guida di MBAM 2,5 per i cmdlet di Windows PowerShell dopo l'installazione del software del server MBAM**

1.  Aprire Windows PowerShell o Windows PowerShell Integrated Scripting Environment (ISE).

2.  Digitare **Update-Guida-modulo Microsoft. mbam**.

## <a href="" id="bkmk-help-specific-cmdlet"></a>Come ottenere assistenza per un cmdlet di Windows PowerShell di MBAM


La Guida di Windows PowerShell per MBAM è disponibile nei formati seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato della Guida di Windows PowerShell</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>In un prompt dei comandi di Windows PowerShell digitare <strong> Get-Help </strong> &lt; <em> cmdlet</em>&gt;</p></td>
<td align="left"><p>Per caricare i più recenti cmdlet di Windows PowerShell, seguire le istruzioni della sezione precedente su come caricare la Guida di Windows PowerShell per MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>In TechNet come pagine Web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nell'area download come file di Word. docx</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Nell'area download come file PDF</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a>Configurazioni che è possibile eseguire solo con Windows PowerShell, ma non con la configurazione guidata del server MBAM


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configurazioni che è possibile eseguire solo con Windows PowerShell</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Installare i servizi Web in un computer separato dalle applicazioni Web.</p></td>
<td align="left"><p>Usando la procedura guidata, è necessario installare i servizi Web e le applicazioni Web nello stesso computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Abilitare i report in un punto distinto di Reporting Services senza installare tutti gli oggetti di Configuration Manager.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eliminare tutti gli oggetti da Configuration Manager.</p></td>
<td align="left"><p>L'eliminazione degli oggetti a sua volta Elimina tutti i dati di conformità da Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Immettere una stringa di connessione personalizzata per i database.</p></td>
<td align="left"><p>Esempio: per configurare le applicazioni Web in modo che funzionino con il mirroring, devi usare il <strong> cmdlet Enable-MbamWebApplication </strong> per specificare la sintassi appropriata per i partner di failover nella stringa di connessione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ignorare la convalida e configurare una caratteristica anche se il controllo dei prerequisiti non è riuscito.</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

**Nota**  Non è possibile disabilitare i database MBAM con un cmdlet di Windows PowerShell o con la configurazione guidata del server MBAM. Per impedire la rimozione accidentale dei dati di conformità e di controllo, gli amministratori di database devono rimuovere manualmente i database.

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a>Prerequisiti e requisiti per l'uso di Windows PowerShell per configurare le caratteristiche del server MBAM


Prima di avviare la configurazione, completare i prerequisiti seguenti.

**Prerequisiti relativi agli account**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti</th>
<th align="left">Dettagli o altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Creare gli account necessari.</p></td>
<td align="left"><p>Vedere <strong> la sezione account necessari e i parametri del cmdlet di Windows PowerShell corrispondenti </strong> più avanti in questo argomento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gli account utente e i gruppi passati come parametri ai cmdlet di Windows PowerShell devono essere account validi nel dominio.</p></td>
<td align="left"><p>Non è possibile usare gli account locali.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Specificare gli account nel formato di livello più basso.</p></td>
<td align="left"><p>Esempi:</p>
<p>domainNetBiosName\userdomainNetBiosName\group</p></td>
</tr>
</tbody>
</table>

 

**Prerequisiti relativi alle autorizzazioni**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti</th>
<th align="left">Dettagli o altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>È necessario essere un amministratore nel computer locale in cui si sta configurando la caratteristica MBAM.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Usare un prompt dei comandi di Windows PowerShell con privilegi elevati per eseguire tutti i cmdlet di Windows PowerShell.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Solo per il <strong> cmdlet Enable-MbamDatabase </strong> :</p>
<p>&quot; &quot; Per l'istanza del database di Microsoft SQL Server di destinazione è necessario aver creato le autorizzazioni per il database.</p>
<p>Questo account utente deve far parte del gruppo Administrators locale o del gruppo Backup Operators per registrare il writer del servizio Copia Shadow del volume di MBAM (VSS).</p></td>
<td align="left"><p>Per impostazione predefinita, l'amministratore del database o l'amministratore di sistema ha le autorizzazioni necessarie per &quot; creare qualsiasi database &quot; .</p>
<p></p>
<p>Per altre informazioni su VSS Writer, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> servizio Copia Shadow del volume </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Solo per la <strong> funzionalità di integrazione di System Center Configuration Manager </strong> :</p>
<p>L'utente che abilita questa funzionalità deve avere questi diritti in Configuration Manager:</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo di diritti in Configuration Manager</th>
<th align="left">Diritti obbligatori</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Diritti sito di Configuration Manager:</p></td>
<td align="left"><p>- Read</p></td>
</tr>
<tr class="even">
<td align="left"><p>Diritti di raccolta di Configuration Manager:</p></td>
<td align="left"><p>- Crea-Elimina-leggi-modifica-Distribuisci elementi di configurazione</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Diritti degli elementi di configurazione di Configuration Manager:</p></td>
<td align="left"><p>- Crea-Elimina-leggi</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a>Uso di Windows PowerShell per configurare MBAM in un computer remoto


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Quando usare questa funzionalità</strong></p></td>
<td align="left"><p>Quando si vogliono configurare le caratteristiche del server MBAM 2,5 in un computer remoto. I cmdlet di Windows PowerShell sono in uso in un computer e si configurano le caratteristiche in un computer remoto diverso.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Operazioni da eseguire</strong></p></td>
<td align="left"><p>Per usare Windows PowerShell per configurare le caratteristiche del server MBAM 2,5 in un computer remoto, è necessario:</p>
<ul>
<li><p>Verificare che il software MBAM 2,5 Server sia stato installato nel computer remoto.</p></li>
<li><p>Usare il protocollo CredSSP (Credential Security Support Provider) per aprire la sessione di Windows PowerShell.</p></li>
<li><p>Abilitare Gestione remota Windows (WinRM). Se non si riesce a abilitare WinRM e a configurarlo correttamente, il <strong> cmdlet New-PSSession </strong> descritto in questa tabella mostra un errore e descrive come risolvere il problema. Per altre informazioni su WinRM, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> uso di gestione remota di Windows </a> .</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Perché è necessario farlo</strong></p></td>
<td align="left"><p>Questo protocollo consente ai cmdlet di Windows PowerShell di connettersi a servizi di dominio Active Directory utilizzando le credenziali amministrative dell'utente. Potrebbe essere visualizzato un errore di convalida se si avvia la sessione di Windows PowerShell senza questo protocollo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Come avviare una sessione di Windows PowerShell con il protocollo CredSSP</strong></p></td>
<td align="left"><p>Digitare il codice seguente al prompt di Windows PowerShell:</p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p>Il codice seguente mostra un esempio.</p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a>Account obbligatori e parametri del cmdlet di Windows PowerShell corrispondenti


La tabella seguente descrive gli account necessari per configurare le caratteristiche del server MBAM 2,5. Vengono inoltre elencati i cmdlet e il parametro di Windows PowerShell corrispondente per cui è necessario specificare l'account durante la configurazione.

Tipo di parametro cmdlet (utente o gruppo) Descrizione Enable-MBAMDatabase

AccessAccount

Utente o gruppo

Specificare un utente o un gruppo di dominio che disponga dell'autorizzazione di lettura/scrittura per il database per consentire alle applicazioni Web di accedere ai dati e ai report nel database. Se il valore è un utente di dominio, il parametro **WebServiceApplicationPoolCredential** usato quando si usa il cmdlet **Enable-MbamWebApplication** deve usare lo stesso account utente. Se il valore è un gruppo Domain Users, l'account di dominio usato dal parametro **WebServiceApplicationPoolCredential** deve essere un membro di questo gruppo.

ReportAccount

Utente o gruppo

Specificare un utente o un gruppo di utenti di dominio che disponga dell'autorizzazione di sola lettura per il database per consentire ai report di MBAM di accedere ai dati di conformità e controllo. Se il valore è un utente di dominio, il parametro **ComplianceAndAuditDBCredential** del cmdlet **Enable-MbamReport** deve usare lo stesso account utente. Se il valore è un gruppo Domain Users, l'account di dominio usato dal parametro **ComplianceAndAuditDBCredential** deve essere un membro di questo gruppo.

Enable-MbamReport

ComplianceAndAuditDBCredential

Utente

Specifica le credenziali amministrative usate dall'istanza SSRS locale per connettersi al database di controllo e conformità di MBAM. L'utente del dominio nelle credenziali amministrative deve essere uguale all'account utente usato per il parametro **ReportAccount** , che viene usato durante l'esecuzione del cmdlet **Enable-MbamDatabase** . Se un gruppo Domain Users è stato usato con il parametro **ReportAccount** , questo account deve essere un membro del gruppo.

**Importante**  L'account specificato nelle credenziali amministrative deve avere diritti utente limitati per migliorare la sicurezza. La password dell'account deve inoltre essere impostata su not expire.

 

ReportsReadOnlyAccessGroup

Gruppo

Specifica il gruppo di utenti del dominio con autorizzazioni di lettura per i report. Il gruppo specificato deve essere lo stesso gruppo usato per il parametro **ReportsReadOnlyAccessGroup** nel cmdlet **Enable-MbamWebApplication** .

Enable-MBAMWebApplication

AdvancedHelpdeskAccessGroup

Gruppo

Specifica il gruppo Domain Users che ha accesso a tutte le aree del sito Web di amministrazione e monitoraggio, ad eccezione dell'area report.

HelpdeskAccessGroup

Gruppo

Specifica il gruppo Domain Users che ha accesso alle aree di **Gestione TPM** e **recupero unità** del sito Web amministrazione e monitoraggio.

ReportsReadOnlyAccessGroup

Gruppo

Specifica il gruppo Domain Users che ha l'autorizzazione di lettura per l'area **report** del sito Web di amministrazione e monitoraggio. Il gruppo specificato deve essere lo stesso gruppo usato per il parametro **ReportsReadOnlyAccessGroup** nel cmdlet **Enable-MbamReport** .

WebServiceApplicationPoolCredential

Utente

Specifica l'utente del dominio che deve essere usato dal pool di applicazioni per le applicazioni Web di MBAM. Deve essere lo stesso account utente di dominio specificato nel parametro **AccessAccount** del cmdlet **Enable-MbamDatabase** . Se un gruppo di utenti di dominio è stato usato dal parametro **AccessAccount** durante l'uso del cmdlet **Enable-MbamDatabase** , l'utente del dominio specificato qui deve essere un membro del gruppo. Se non specifichi le credenziali amministrative, vengono usate le credenziali amministrative specificate da qualsiasi applicazione Web abilitata in precedenza. Tutte le applicazioni Web usano la stessa identità del pool di applicazioni. Se viene specificato più volte, viene usato il valore specificato più di recente.

**Importante**  Per una maggiore sicurezza, imposta l'account specificato nelle credenziali amministrative per limitare i diritti utente. Imposta inoltre la password dell'account su non scadono mai. Verificare che l'account predefinito IIS \ _IUSRS o l'account usato per il parametro **WebServiceApplicationPoolCredential** sia stato aggiunto al **client Impersonate dopo** l'impostazione di sicurezza locale di autenticazione.

Per visualizzare l'impostazione di sicurezza locale, aprire l' **Editor criteri di sicurezza locali**, espandere il nodo **criteri locali** , selezionare il nodo **assegnazione diritti utente** e quindi fare doppio clic sul pulsante **rappresenta un client dopo l'autenticazione** e **accedere come** impostazioni di criteri di gruppo processo batch nel riquadro dei dettagli.

 

 




## Argomenti correlati


[Configurazione delle funzionalità server di MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Convalida della configurazione delle funzionalità del server di MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)

[Uso di Windows PowerShell per l'amministrazione di MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md)

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





